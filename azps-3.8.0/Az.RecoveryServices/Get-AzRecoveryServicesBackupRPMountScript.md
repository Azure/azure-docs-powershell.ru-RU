---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 427da45eed5e2e9e27421e67d9e6e776d9106367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074731"
---
# <span data-ttu-id="f316b-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="f316b-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="f316b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f316b-102">SYNOPSIS</span></span>
<span data-ttu-id="f316b-103">Загружает сценарий для присоединения всех файлов точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="f316b-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="f316b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f316b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f316b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f316b-105">DESCRIPTION</span></span>
<span data-ttu-id="f316b-106">Командлет Get-AzRecoveryServicesBackupRPMountScript загружает сценарий, который подключает тома точки восстановления на компьютере, на котором она выполняется.</span><span class="sxs-lookup"><span data-stu-id="f316b-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="f316b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f316b-107">EXAMPLES</span></span>

### <span data-ttu-id="f316b-108">Пример 1: подключение точки восстановления</span><span class="sxs-lookup"><span data-stu-id="f316b-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="f316b-109">При запуске сценария файлы точки восстановления будут подключены $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="f316b-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="f316b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f316b-110">PARAMETERS</span></span>

### <span data-ttu-id="f316b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f316b-111">-DefaultProfile</span></span>
<span data-ttu-id="f316b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f316b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f316b-113">-Path</span><span class="sxs-lookup"><span data-stu-id="f316b-113">-Path</span></span>
<span data-ttu-id="f316b-114">Место, где должен быть загружен файл, в случае восстановления файла.</span><span class="sxs-lookup"><span data-stu-id="f316b-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="f316b-115">Если не указан путь, файл сценария будет загружен в текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="f316b-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f316b-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f316b-116">-RecoveryPoint</span></span>
<span data-ttu-id="f316b-117">Восстанавливаемый объект точки восстановления</span><span class="sxs-lookup"><span data-stu-id="f316b-117">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f316b-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f316b-118">-VaultId</span></span>
<span data-ttu-id="f316b-119">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f316b-119">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f316b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f316b-120">-Confirm</span></span>
<span data-ttu-id="f316b-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f316b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f316b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f316b-122">-WhatIf</span></span>
<span data-ttu-id="f316b-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f316b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f316b-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f316b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f316b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f316b-125">CommonParameters</span></span>
<span data-ttu-id="f316b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f316b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f316b-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f316b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f316b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f316b-128">INPUTS</span></span>

### <span data-ttu-id="f316b-129">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f316b-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="f316b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f316b-130">System.String</span></span>

## <span data-ttu-id="f316b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f316b-131">OUTPUTS</span></span>

### <span data-ttu-id="f316b-132">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="f316b-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="f316b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f316b-133">NOTES</span></span>

## <span data-ttu-id="f316b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f316b-134">RELATED LINKS</span></span>
