---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 2613761db4a975f1bd4e04458ccdc5df81c0a2d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729761"
---
# <span data-ttu-id="98911-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="98911-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="98911-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98911-102">SYNOPSIS</span></span>
<span data-ttu-id="98911-103">Отключение автоматического резервного копирования для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="98911-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="98911-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98911-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98911-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98911-105">DESCRIPTION</span></span>
<span data-ttu-id="98911-106">Командлет **Disable-AzRecoveryServicesBackupAutoProtection** отключает защиту для защищаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="98911-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="98911-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98911-107">EXAMPLES</span></span>

### <span data-ttu-id="98911-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98911-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="98911-109">Первый командлет отключает политику защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="98911-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="98911-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98911-110">PARAMETERS</span></span>

### <span data-ttu-id="98911-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="98911-111">-BackupManagementType</span></span>
<span data-ttu-id="98911-112">Тип управления резервным копированием ресурса (например: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="98911-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98911-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98911-113">-DefaultProfile</span></span>
<span data-ttu-id="98911-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98911-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98911-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="98911-115">-InputItem</span></span>
<span data-ttu-id="98911-116">Идентификатор элемента</span><span class="sxs-lookup"><span data-stu-id="98911-116">Item Id</span></span>

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

### <span data-ttu-id="98911-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98911-117">-PassThru</span></span>
<span data-ttu-id="98911-118">Возвращают результат для автоматического обеспечения защиты.</span><span class="sxs-lookup"><span data-stu-id="98911-118">Return the result for auto protection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98911-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="98911-119">-VaultId</span></span>
<span data-ttu-id="98911-120">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="98911-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98911-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="98911-121">-WorkloadType</span></span>
<span data-ttu-id="98911-122">Тип рабочей нагрузки ресурса (например,: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="98911-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98911-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98911-123">-Confirm</span></span>
<span data-ttu-id="98911-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98911-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98911-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98911-125">-WhatIf</span></span>
<span data-ttu-id="98911-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98911-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98911-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98911-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98911-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98911-128">CommonParameters</span></span>
<span data-ttu-id="98911-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98911-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="98911-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98911-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98911-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98911-131">INPUTS</span></span>

### <span data-ttu-id="98911-132">System. String</span><span class="sxs-lookup"><span data-stu-id="98911-132">System.String</span></span>

## <span data-ttu-id="98911-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98911-133">OUTPUTS</span></span>

### <span data-ttu-id="98911-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98911-134">System.Boolean</span></span>

## <span data-ttu-id="98911-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="98911-135">NOTES</span></span>

## <span data-ttu-id="98911-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98911-136">RELATED LINKS</span></span>
