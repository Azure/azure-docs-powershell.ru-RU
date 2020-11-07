---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 97eae8c5c545297a7d6287a951ec02433d591168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912791"
---
# <span data-ttu-id="349c0-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="349c0-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="349c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="349c0-102">SYNOPSIS</span></span>
<span data-ttu-id="349c0-103">Отключение автоматического резервного копирования для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="349c0-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="349c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="349c0-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="349c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="349c0-105">DESCRIPTION</span></span>
<span data-ttu-id="349c0-106">Командлет **Disable-AzRecoveryServicesBackupAutoProtection** отключает защиту для защищаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="349c0-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="349c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="349c0-107">EXAMPLES</span></span>

### <span data-ttu-id="349c0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="349c0-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="349c0-109">Первый командлет отключает политику защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="349c0-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="349c0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="349c0-110">PARAMETERS</span></span>

### <span data-ttu-id="349c0-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="349c0-111">-BackupManagementType</span></span>
<span data-ttu-id="349c0-112">Тип управления резервным копированием ресурса (например: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="349c0-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349c0-113">-DefaultProfile</span></span>
<span data-ttu-id="349c0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="349c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="349c0-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="349c0-115">-InputItem</span></span>
<span data-ttu-id="349c0-116">Идентификатор элемента</span><span class="sxs-lookup"><span data-stu-id="349c0-116">Item Id</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="349c0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="349c0-117">-PassThru</span></span>
<span data-ttu-id="349c0-118">Возвращают результат для автоматического обеспечения защиты.</span><span class="sxs-lookup"><span data-stu-id="349c0-118">Return the result for auto protection.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c0-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="349c0-119">-VaultId</span></span>
<span data-ttu-id="349c0-120">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="349c0-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="349c0-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="349c0-121">-WorkloadType</span></span>
<span data-ttu-id="349c0-122">Тип рабочей нагрузки ресурса (например,: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="349c0-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="349c0-123">-Confirm</span></span>
<span data-ttu-id="349c0-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="349c0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="349c0-125">-WhatIf</span></span>
<span data-ttu-id="349c0-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="349c0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="349c0-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="349c0-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349c0-128">CommonParameters</span></span>
<span data-ttu-id="349c0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="349c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349c0-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="349c0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349c0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="349c0-131">INPUTS</span></span>

### <span data-ttu-id="349c0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="349c0-132">System.String</span></span>

## <span data-ttu-id="349c0-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="349c0-133">OUTPUTS</span></span>

### <span data-ttu-id="349c0-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="349c0-134">System.Boolean</span></span>

## <span data-ttu-id="349c0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="349c0-135">NOTES</span></span>

## <span data-ttu-id="349c0-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="349c0-136">RELATED LINKS</span></span>
