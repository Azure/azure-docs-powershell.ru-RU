---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904869"
---
# <span data-ttu-id="c3115-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="c3115-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="c3115-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3115-102">SYNOPSIS</span></span>
<span data-ttu-id="c3115-103">Создает объект сопоставления дисков для реплицируемых дисков виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="c3115-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="c3115-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3115-104">SYNTAX</span></span>

### <span data-ttu-id="c3115-105">AzureToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3115-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3115-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c3115-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3115-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3115-107">DESCRIPTION</span></span>
<span data-ttu-id="c3115-108">Создает объект сопоставления дисков, который сопоставляет диск виртуальной машины Azure с учетной записью хранения кэша и целевой учетной записью хранилища (областью восстановления), которая будет использоваться для репликации диска.</span><span class="sxs-lookup"><span data-stu-id="c3115-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="c3115-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3115-109">EXAMPLES</span></span>

### <span data-ttu-id="c3115-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3115-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="c3115-111">Создайте объект сопоставления дисков для дисков виртуальных машин Azure, которые нужно реплицировать. Используется во время работы Azure для Azure и повторной защиты.</span><span class="sxs-lookup"><span data-stu-id="c3115-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="c3115-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3115-112">PARAMETERS</span></span>

### <span data-ttu-id="c3115-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3115-113">-DefaultProfile</span></span>
<span data-ttu-id="c3115-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3115-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3115-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="c3115-115">-DiskId</span></span>
<span data-ttu-id="c3115-116">Указывает идентификатор диска управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="c3115-116">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3115-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c3115-117">-LogStorageAccountId</span></span>
<span data-ttu-id="c3115-118">Указывает идентификатор журнала или учетной записи для хранения кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="c3115-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3115-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c3115-119">-ManagedDisk</span></span>
<span data-ttu-id="c3115-120">Указывает входные данные для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="c3115-120">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3115-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c3115-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="c3115-122">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="c3115-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3115-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="c3115-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="c3115-124">Указывает тип учетной записи реплицированного управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="c3115-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3115-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c3115-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="c3115-126">Указывает идентификатор группы ресурсов восстановления для реплицируемого управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="c3115-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3115-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="c3115-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="c3115-128">Указывает конечный диск восстановления для реплицируемого управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="c3115-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3115-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="c3115-129">-VhdUri</span></span>
<span data-ttu-id="c3115-130">Укажите URI виртуального жесткого диска, которому соответствует это сопоставление.</span><span class="sxs-lookup"><span data-stu-id="c3115-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3115-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3115-131">-Confirm</span></span>
<span data-ttu-id="c3115-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c3115-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3115-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3115-133">-WhatIf</span></span>
<span data-ttu-id="c3115-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c3115-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3115-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c3115-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3115-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3115-136">CommonParameters</span></span>
<span data-ttu-id="c3115-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3115-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3115-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3115-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3115-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3115-139">INPUTS</span></span>

### <span data-ttu-id="c3115-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="c3115-140">None</span></span>

## <span data-ttu-id="c3115-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3115-141">OUTPUTS</span></span>

### <span data-ttu-id="c3115-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="c3115-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="c3115-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3115-143">NOTES</span></span>

## <span data-ttu-id="c3115-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3115-144">RELATED LINKS</span></span>
