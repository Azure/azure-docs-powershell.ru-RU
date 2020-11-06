---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: bfcd198cd629c9b5f1cd37d3d144bc810a6f4b37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558964"
---
# <span data-ttu-id="f29ed-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="f29ed-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="f29ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f29ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f29ed-103">Отключение всех файлов точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="f29ed-103">Dismounts all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f29ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f29ed-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f29ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f29ed-105">DESCRIPTION</span></span>
<span data-ttu-id="f29ed-106">Командлет Disable-AzureRmRecoveryServicesBackupRPMountScript размонтирует файлы точки восстановления, которые были подключены ранее с помощью командлета Get-AzureRmRecoveryServicesBackupRPMountScript.</span><span class="sxs-lookup"><span data-stu-id="f29ed-106">The Disable-AzureRmRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="f29ed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f29ed-107">EXAMPLES</span></span>

### <span data-ttu-id="f29ed-108">Пример 1: отключение точки восстановления</span><span class="sxs-lookup"><span data-stu-id="f29ed-108">Example 1: Dismount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="f29ed-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f29ed-109">PARAMETERS</span></span>

### <span data-ttu-id="f29ed-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29ed-110">-DefaultProfile</span></span>
<span data-ttu-id="f29ed-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f29ed-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29ed-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f29ed-112">-PassThru</span></span>
<span data-ttu-id="f29ed-113">Возвращает точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="f29ed-113">Return the recovery point.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29ed-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f29ed-114">-RecoveryPoint</span></span>
<span data-ttu-id="f29ed-115">Восстанавливаемый объект точки восстановления</span><span class="sxs-lookup"><span data-stu-id="f29ed-115">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f29ed-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f29ed-116">-Confirm</span></span>
<span data-ttu-id="f29ed-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f29ed-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29ed-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f29ed-118">-WhatIf</span></span>
<span data-ttu-id="f29ed-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f29ed-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f29ed-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f29ed-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29ed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29ed-121">CommonParameters</span></span>
<span data-ttu-id="f29ed-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f29ed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29ed-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f29ed-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29ed-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f29ed-124">INPUTS</span></span>

### <span data-ttu-id="f29ed-125">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f29ed-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="f29ed-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f29ed-126">OUTPUTS</span></span>

### <span data-ttu-id="f29ed-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="f29ed-127">System.Object</span></span>

## <span data-ttu-id="f29ed-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f29ed-128">NOTES</span></span>

## <span data-ttu-id="f29ed-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f29ed-129">RELATED LINKS</span></span>

