---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074708"
---
# <span data-ttu-id="7d57c-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d57c-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="7d57c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d57c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d57c-103">Эта команда запускает обнаружение незащищенных элементов заданного типа рабочей нагрузки в заданном контейнере.</span><span class="sxs-lookup"><span data-stu-id="7d57c-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="7d57c-104">Если приложение DB не защищено автоматически, используйте эту команду, чтобы найти новый DBs, когда они будут добавлены, и продолжите их защиту.</span><span class="sxs-lookup"><span data-stu-id="7d57c-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="7d57c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d57c-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d57c-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d57c-106">DESCRIPTION</span></span>
<span data-ttu-id="7d57c-107">Командлет зазапрос для определенных рабочих нагрузок в контейнере.</span><span class="sxs-lookup"><span data-stu-id="7d57c-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="7d57c-108">Это вызывает операцию, которая создает защищенные элементы.</span><span class="sxs-lookup"><span data-stu-id="7d57c-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="7d57c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d57c-109">EXAMPLES</span></span>

### <span data-ttu-id="7d57c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d57c-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="7d57c-111">Командлет выполняет операцию обнаружения для новых защищенных элементов.</span><span class="sxs-lookup"><span data-stu-id="7d57c-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="7d57c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d57c-112">PARAMETERS</span></span>

### <span data-ttu-id="7d57c-113">-Container</span><span class="sxs-lookup"><span data-stu-id="7d57c-113">-Container</span></span>
<span data-ttu-id="7d57c-114">Контейнер, в котором находится элемент</span><span class="sxs-lookup"><span data-stu-id="7d57c-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d57c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d57c-115">-DefaultProfile</span></span>
<span data-ttu-id="7d57c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d57c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d57c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d57c-117">-PassThru</span></span>
<span data-ttu-id="7d57c-118">Возвращает контейнер, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7d57c-118">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="7d57c-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7d57c-119">-VaultId</span></span>
<span data-ttu-id="7d57c-120">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7d57c-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7d57c-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7d57c-121">-WorkloadType</span></span>
<span data-ttu-id="7d57c-122">Тип рабочей нагрузки ресурса (например,: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="7d57c-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d57c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d57c-123">-Confirm</span></span>
<span data-ttu-id="7d57c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d57c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d57c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d57c-125">-WhatIf</span></span>
<span data-ttu-id="7d57c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d57c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d57c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d57c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d57c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d57c-128">CommonParameters</span></span>
<span data-ttu-id="7d57c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d57c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d57c-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d57c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d57c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d57c-131">INPUTS</span></span>

### <span data-ttu-id="7d57c-132">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="7d57c-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="7d57c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7d57c-133">System.String</span></span>

## <span data-ttu-id="7d57c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d57c-134">OUTPUTS</span></span>

### <span data-ttu-id="7d57c-135">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="7d57c-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="7d57c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d57c-136">NOTES</span></span>

## <span data-ttu-id="7d57c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d57c-137">RELATED LINKS</span></span>
