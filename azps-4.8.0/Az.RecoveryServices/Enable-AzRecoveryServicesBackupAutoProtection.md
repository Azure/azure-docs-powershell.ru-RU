---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234799"
---
# <span data-ttu-id="9b5d3-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="9b5d3-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="9b5d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5d3-103">Командлет **Enable-AzRecoveryServicesBackupAutoProtection** настраивает автоматическую защиту текущих и всех будущих DBs SQL в рамках данного экземпляра с помощью предоставленной политики.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="9b5d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b5d3-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b5d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b5d3-105">DESCRIPTION</span></span>
<span data-ttu-id="9b5d3-106">Эта команда позволяет пользователям автоматически защищать все существующие незащищенные SQL DBs и любые базы данных, которые будут добавлены позже с помощью заданной политики.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="9b5d3-107">Так как инструкция будет создавать резервные копии всех будущих DBs, операция выполняется на уровне SQLInstance, служба архивации Azure будет периодически проверять автоматически защищенные контейнеры для новых DBs и автоматически защищать их.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="9b5d3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b5d3-108">EXAMPLES</span></span>

### <span data-ttu-id="9b5d3-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b5d3-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="9b5d3-110">Первый командлет получает объект политики по умолчанию, а затем сохраняет его в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="9b5d3-111">Второй командлет извлекает подходящую SQLInstance, которая является защищаемым элементом.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="9b5d3-112">Затем третья команда настраивает автоматическую защиту для этого экземпляра с помощью политики в $Pol.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="9b5d3-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9b5d3-113">Example 2</span></span>

<span data-ttu-id="9b5d3-114">Эти команды позволяют пользователям автоматически защищать все существующие незащищенные DBs и любые базы данных, которые будут добавлены позже с помощью заданной политики.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="9b5d3-115">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="9b5d3-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="9b5d3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b5d3-116">PARAMETERS</span></span>

### <span data-ttu-id="9b5d3-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9b5d3-117">-BackupManagementType</span></span>
<span data-ttu-id="9b5d3-118">Класс защищаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-118">The class of resources being protected.</span></span> <span data-ttu-id="9b5d3-119">В настоящее время поддерживаются следующие значения для этого командлета — MAB, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="9b5d3-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

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

### <span data-ttu-id="9b5d3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5d3-120">-DefaultProfile</span></span>
<span data-ttu-id="9b5d3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b5d3-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="9b5d3-122">-InputItem</span></span>
<span data-ttu-id="9b5d3-123">Указывает объект с защитой элемента, который можно передать в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="9b5d3-124">Текущее поддерживаемое значение — объект protectableItem типа "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="9b5d3-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

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

### <span data-ttu-id="9b5d3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b5d3-125">-PassThru</span></span>
<span data-ttu-id="9b5d3-126">Возвращают результат для автоматического обеспечения защиты.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="9b5d3-127">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="9b5d3-127">-Policy</span></span>
<span data-ttu-id="9b5d3-128">Объект политики защиты.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-128">Protection policy object.</span></span>

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

### <span data-ttu-id="9b5d3-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9b5d3-129">-VaultId</span></span>
<span data-ttu-id="9b5d3-130">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9b5d3-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="9b5d3-131">-WorkloadType</span></span>
<span data-ttu-id="9b5d3-132">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-132">Workload type of the resource.</span></span> <span data-ttu-id="9b5d3-133">Текущие поддерживаемые значения — AzureVM, WindowsServer, MSSQL.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

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

### <span data-ttu-id="9b5d3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b5d3-134">-Confirm</span></span>
<span data-ttu-id="9b5d3-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b5d3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5d3-136">-WhatIf</span></span>
<span data-ttu-id="9b5d3-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="9b5d3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5d3-138">CommonParameters</span></span>
<span data-ttu-id="9b5d3-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5d3-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b5d3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5d3-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b5d3-141">INPUTS</span></span>

### <span data-ttu-id="9b5d3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9b5d3-142">System.String</span></span>

## <span data-ttu-id="9b5d3-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b5d3-143">OUTPUTS</span></span>

### <span data-ttu-id="9b5d3-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="9b5d3-144">System.Object</span></span>

## <span data-ttu-id="9b5d3-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b5d3-145">NOTES</span></span>

## <span data-ttu-id="9b5d3-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b5d3-146">RELATED LINKS</span></span>
