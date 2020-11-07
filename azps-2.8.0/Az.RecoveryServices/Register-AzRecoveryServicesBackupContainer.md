---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: eeffbbd62a4c161b95004c6f4bd40d31fbd02517
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905858"
---
# <span data-ttu-id="053f5-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="053f5-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="053f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="053f5-102">SYNOPSIS</span></span>
<span data-ttu-id="053f5-103">Эта команда позволяет службе архивации Azure преобразовать ресурс в контейнер резервного копирования, который затем регистрируется в заданном хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="053f5-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="053f5-104">Служба архивации Azure может затем найти в этом контейнере рабочие нагрузки указанного типа рабочей нагрузки для более поздней защиты.</span><span class="sxs-lookup"><span data-stu-id="053f5-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="053f5-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="053f5-105">SYNTAX</span></span>

### <span data-ttu-id="053f5-106">Регистрация (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="053f5-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="053f5-107">Повторная регистрация</span><span class="sxs-lookup"><span data-stu-id="053f5-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="053f5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="053f5-108">DESCRIPTION</span></span>
<span data-ttu-id="053f5-109">Командлет регистрирует виртуальную машину Azure для AzureWorkloads с определенными workloadType.</span><span class="sxs-lookup"><span data-stu-id="053f5-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="053f5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="053f5-110">EXAMPLES</span></span>

### <span data-ttu-id="053f5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="053f5-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="053f5-112">Командлет регистрирует ВМ Azure для рабочей нагрузки MSSQL.</span><span class="sxs-lookup"><span data-stu-id="053f5-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="053f5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="053f5-113">PARAMETERS</span></span>

### <span data-ttu-id="053f5-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="053f5-114">-BackupManagementType</span></span>
<span data-ttu-id="053f5-115">Тип управления резервным копированием контейнера резервной копии Azure</span><span class="sxs-lookup"><span data-stu-id="053f5-115">The backup management type of the Azure Backup container</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="053f5-116">-Container</span><span class="sxs-lookup"><span data-stu-id="053f5-116">-Container</span></span>
<span data-ttu-id="053f5-117">Контейнер, в котором находится элемент</span><span class="sxs-lookup"><span data-stu-id="053f5-117">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="053f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="053f5-118">-DefaultProfile</span></span>
<span data-ttu-id="053f5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="053f5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="053f5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="053f5-120">-Force</span></span>
<span data-ttu-id="053f5-121">Обязательное использование контейнера регистров (диалоговое окно подтверждения не задается).</span><span class="sxs-lookup"><span data-stu-id="053f5-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="053f5-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="053f5-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="053f5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="053f5-123">-ResourceId</span></span>
<span data-ttu-id="053f5-124">Идентификатор ресурса Azure, элемент которого должен быть проверен, если он уже защищен некоторым хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="053f5-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="053f5-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="053f5-125">-VaultId</span></span>
<span data-ttu-id="053f5-126">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="053f5-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="053f5-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="053f5-127">-WorkloadType</span></span>
<span data-ttu-id="053f5-128">Тип рабочей нагрузки ресурса (например,: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="053f5-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="053f5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="053f5-129">-Confirm</span></span>
<span data-ttu-id="053f5-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="053f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="053f5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="053f5-131">-WhatIf</span></span>
<span data-ttu-id="053f5-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="053f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="053f5-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="053f5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="053f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="053f5-134">CommonParameters</span></span>
<span data-ttu-id="053f5-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="053f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="053f5-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="053f5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="053f5-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="053f5-137">INPUTS</span></span>

### <span data-ttu-id="053f5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="053f5-138">System.String</span></span>

## <span data-ttu-id="053f5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="053f5-139">OUTPUTS</span></span>

### <span data-ttu-id="053f5-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="053f5-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="053f5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="053f5-141">NOTES</span></span>

## <span data-ttu-id="053f5-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="053f5-142">RELATED LINKS</span></span>