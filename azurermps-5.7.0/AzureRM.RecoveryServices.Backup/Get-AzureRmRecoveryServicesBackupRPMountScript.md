---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 0f3f0292b4f348207bf80d5e04c63dc45be69fa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558940"
---
# <span data-ttu-id="b787b-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="b787b-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="b787b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b787b-102">SYNOPSIS</span></span>
<span data-ttu-id="b787b-103">Загружает сценарий для присоединения всех файлов точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="b787b-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b787b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b787b-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b787b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b787b-105">DESCRIPTION</span></span>
<span data-ttu-id="b787b-106">Командлет Get-AzureRmRecoveryServicesBackupRPMountScript загружает сценарий, который подключает тома точки восстановления на компьютере, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="b787b-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="b787b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b787b-107">EXAMPLES</span></span>

### <span data-ttu-id="b787b-108">Пример 1: подключение точки восстановления</span><span class="sxs-lookup"><span data-stu-id="b787b-108">Example 1: Mount a recovery point</span></span>
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
```

<span data-ttu-id="b787b-109">При запуске сценария файлы точки восстановления будут подключены $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="b787b-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="b787b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b787b-110">PARAMETERS</span></span>

### <span data-ttu-id="b787b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b787b-111">-DefaultProfile</span></span>
<span data-ttu-id="b787b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b787b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b787b-113">-Path</span><span class="sxs-lookup"><span data-stu-id="b787b-113">-Path</span></span>
<span data-ttu-id="b787b-114">Место, где должен быть загружен файл, в случае восстановления файла.</span><span class="sxs-lookup"><span data-stu-id="b787b-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="b787b-115">Если не указан путь, файл сценария будет загружен в текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="b787b-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b787b-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b787b-116">-RecoveryPoint</span></span>
<span data-ttu-id="b787b-117">Восстанавливаемый объект точки восстановления</span><span class="sxs-lookup"><span data-stu-id="b787b-117">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="b787b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b787b-118">-Confirm</span></span>
<span data-ttu-id="b787b-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b787b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b787b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b787b-120">-WhatIf</span></span>
<span data-ttu-id="b787b-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b787b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b787b-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b787b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b787b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b787b-123">CommonParameters</span></span>
<span data-ttu-id="b787b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b787b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b787b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b787b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b787b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b787b-126">INPUTS</span></span>

### <span data-ttu-id="b787b-127">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b787b-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b787b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b787b-128">OUTPUTS</span></span>

### <span data-ttu-id="b787b-129">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="b787b-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="b787b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b787b-130">NOTES</span></span>

## <span data-ttu-id="b787b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b787b-131">RELATED LINKS</span></span>

