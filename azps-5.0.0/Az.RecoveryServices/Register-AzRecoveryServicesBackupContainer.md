---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248049"
---
# <span data-ttu-id="471d6-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="471d6-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="471d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="471d6-102">SYNOPSIS</span></span>
<span data-ttu-id="471d6-103">Командлет **Register-AzRecoveryServicesBackupContainer** регистрирует виртуальную машину Azure для AzureWorkloads с определенным workloadType.</span><span class="sxs-lookup"><span data-stu-id="471d6-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="471d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="471d6-104">SYNTAX</span></span>

### <span data-ttu-id="471d6-105">Регистрация (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="471d6-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="471d6-106">Повторная регистрация</span><span class="sxs-lookup"><span data-stu-id="471d6-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="471d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="471d6-107">DESCRIPTION</span></span>
<span data-ttu-id="471d6-108">Эта команда позволяет службе архивации Azure преобразовать ресурс в контейнер резервного копирования, который затем регистрируется в заданном хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="471d6-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="471d6-109">Служба архивации Azure может затем найти в этом контейнере рабочие нагрузки указанного типа рабочей нагрузки для более поздней защиты.</span><span class="sxs-lookup"><span data-stu-id="471d6-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="471d6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="471d6-110">EXAMPLES</span></span>

### <span data-ttu-id="471d6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="471d6-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="471d6-112">Командлет регистрирует виртуальную машину Azure в качестве контейнера для рабочей нагрузки MSSQL.</span><span class="sxs-lookup"><span data-stu-id="471d6-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="471d6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="471d6-113">PARAMETERS</span></span>

### <span data-ttu-id="471d6-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="471d6-114">-BackupManagementType</span></span>
<span data-ttu-id="471d6-115">Класс защищаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="471d6-115">The class of resources being protected.</span></span> <span data-ttu-id="471d6-116">В настоящее время это значение, поддерживаемое для этого командлета, — AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="471d6-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="471d6-117">-Container</span><span class="sxs-lookup"><span data-stu-id="471d6-117">-Container</span></span>
<span data-ttu-id="471d6-118">Контейнер, в котором находится элемент</span><span class="sxs-lookup"><span data-stu-id="471d6-118">Container where the item resides</span></span>

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

### <span data-ttu-id="471d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471d6-119">-DefaultProfile</span></span>
<span data-ttu-id="471d6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="471d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="471d6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="471d6-121">-Force</span></span>
<span data-ttu-id="471d6-122">Обязательное использование контейнера регистров (диалоговое окно подтверждения не задается).</span><span class="sxs-lookup"><span data-stu-id="471d6-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="471d6-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="471d6-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="471d6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="471d6-124">-ResourceId</span></span>
<span data-ttu-id="471d6-125">Идентификатор ресурса Azure, элемент которого должен быть проверен, если он уже защищен некоторым хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="471d6-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="471d6-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="471d6-126">-VaultId</span></span>
<span data-ttu-id="471d6-127">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="471d6-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="471d6-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="471d6-128">-WorkloadType</span></span>
<span data-ttu-id="471d6-129">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="471d6-129">Workload type of the resource.</span></span> <span data-ttu-id="471d6-130">Текущая поддерживаемая стоимость: AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="471d6-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="471d6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="471d6-131">-Confirm</span></span>
<span data-ttu-id="471d6-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="471d6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="471d6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="471d6-133">-WhatIf</span></span>
<span data-ttu-id="471d6-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="471d6-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="471d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471d6-135">CommonParameters</span></span>
<span data-ttu-id="471d6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="471d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471d6-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="471d6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471d6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="471d6-138">INPUTS</span></span>

### <span data-ttu-id="471d6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="471d6-139">System.String</span></span>

## <span data-ttu-id="471d6-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="471d6-140">OUTPUTS</span></span>

### <span data-ttu-id="471d6-141">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="471d6-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="471d6-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="471d6-142">NOTES</span></span>

## <span data-ttu-id="471d6-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="471d6-143">RELATED LINKS</span></span>
