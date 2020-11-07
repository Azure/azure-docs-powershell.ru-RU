---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: a17c7b8addf1bf1218131e8e950185d9da6c22d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729751"
---
# <span data-ttu-id="d53f9-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="d53f9-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="d53f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d53f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d53f9-103">Эти команды позволяют пользователям автоматически защищать все существующие незащищенные DBs и любые базы данных, которые будут добавлены позже с помощью заданной политики.</span><span class="sxs-lookup"><span data-stu-id="d53f9-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="d53f9-104">Затем служба архивации Azure периодически будет проверять автоматически защищенные контейнеры для новых DBs и автоматически защищать их.</span><span class="sxs-lookup"><span data-stu-id="d53f9-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="d53f9-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d53f9-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d53f9-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d53f9-106">DESCRIPTION</span></span>
<span data-ttu-id="d53f9-107">Командлет **Enable-AzRecoveryServicesBackupAutoProtection** задает политику защиты автоматической архивации Azure для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="d53f9-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="d53f9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d53f9-108">EXAMPLES</span></span>

### <span data-ttu-id="d53f9-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d53f9-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="d53f9-110">Первый командлет получает объект политики по умолчанию, а затем сохраняет его в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="d53f9-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="d53f9-111">Второй командлет задает политику защиты резервного копирования для AzureWorkload с помощью политики в $Pol.</span><span class="sxs-lookup"><span data-stu-id="d53f9-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="d53f9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d53f9-112">PARAMETERS</span></span>

### <span data-ttu-id="d53f9-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d53f9-113">-BackupManagementType</span></span>
<span data-ttu-id="d53f9-114">Тип резервного управления для ресурса (например, MAB, DPM, AzureWorkload).</span><span class="sxs-lookup"><span data-stu-id="d53f9-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

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

### <span data-ttu-id="d53f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53f9-115">-DefaultProfile</span></span>
<span data-ttu-id="d53f9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d53f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d53f9-117">-InputItem</span><span class="sxs-lookup"><span data-stu-id="d53f9-117">-InputItem</span></span>
<span data-ttu-id="d53f9-118">Указывает объект с защитой элемента, который можно передать в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="d53f9-118">Specifies the protectable item object that can be passed as an input.</span></span>

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

### <span data-ttu-id="d53f9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d53f9-119">-PassThru</span></span>
<span data-ttu-id="d53f9-120">Возвращают результат для автоматического обеспечения защиты.</span><span class="sxs-lookup"><span data-stu-id="d53f9-120">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="d53f9-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="d53f9-121">-Policy</span></span>
<span data-ttu-id="d53f9-122">Объект политики защиты.</span><span class="sxs-lookup"><span data-stu-id="d53f9-122">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d53f9-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d53f9-123">-VaultId</span></span>
<span data-ttu-id="d53f9-124">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d53f9-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d53f9-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d53f9-125">-WorkloadType</span></span>
<span data-ttu-id="d53f9-126">Тип рабочей нагрузки ресурса (например,: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="d53f9-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="d53f9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d53f9-127">-Confirm</span></span>
<span data-ttu-id="d53f9-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d53f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d53f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d53f9-129">-WhatIf</span></span>
<span data-ttu-id="d53f9-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d53f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d53f9-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d53f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d53f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53f9-132">CommonParameters</span></span>
<span data-ttu-id="d53f9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d53f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53f9-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d53f9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53f9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d53f9-135">INPUTS</span></span>

### <span data-ttu-id="d53f9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d53f9-136">System.String</span></span>

## <span data-ttu-id="d53f9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d53f9-137">OUTPUTS</span></span>

### <span data-ttu-id="d53f9-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="d53f9-138">System.Object</span></span>

## <span data-ttu-id="d53f9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d53f9-139">NOTES</span></span>

## <span data-ttu-id="d53f9-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d53f9-140">RELATED LINKS</span></span>