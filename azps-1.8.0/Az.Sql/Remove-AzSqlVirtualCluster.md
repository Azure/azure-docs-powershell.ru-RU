---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: d4c69457b9932f76d002e3941af3015225345c8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728817"
---
# <span data-ttu-id="8af7d-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="8af7d-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="8af7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8af7d-102">SYNOPSIS</span></span>
<span data-ttu-id="8af7d-103">Удаление виртуального кластера Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8af7d-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="8af7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8af7d-104">SYNTAX</span></span>

### <span data-ttu-id="8af7d-105">RemoveVirtualClusterFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8af7d-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af7d-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="8af7d-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af7d-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8af7d-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af7d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8af7d-108">DESCRIPTION</span></span>
<span data-ttu-id="8af7d-109">Командлет **Remove-AzSqlVirtualCluster** удаляет виртуальный кластер Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8af7d-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="8af7d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8af7d-110">EXAMPLES</span></span>

### <span data-ttu-id="8af7d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8af7d-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="8af7d-112">Эта команда удаляет виртуальный кластер с именем VirtualCluster1, назначенный группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8af7d-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8af7d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8af7d-113">PARAMETERS</span></span>

### <span data-ttu-id="8af7d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8af7d-114">-AsJob</span></span>
<span data-ttu-id="8af7d-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8af7d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8af7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af7d-116">-DefaultProfile</span></span>
<span data-ttu-id="8af7d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8af7d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af7d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8af7d-118">-InputObject</span></span>
<span data-ttu-id="8af7d-119">Объект экземпляра, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8af7d-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8af7d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8af7d-120">-Name</span></span>
<span data-ttu-id="8af7d-121">Имя виртуального кластера.</span><span class="sxs-lookup"><span data-stu-id="8af7d-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8af7d-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8af7d-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af7d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8af7d-124">-ResourceId</span></span>
<span data-ttu-id="8af7d-125">Идентификатор ресурса объекта экземпляра, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8af7d-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af7d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8af7d-126">-Confirm</span></span>
<span data-ttu-id="8af7d-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8af7d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af7d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af7d-128">-WhatIf</span></span>
<span data-ttu-id="8af7d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8af7d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af7d-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8af7d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af7d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af7d-131">CommonParameters</span></span>
<span data-ttu-id="8af7d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8af7d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af7d-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8af7d-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af7d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8af7d-134">INPUTS</span></span>

### <span data-ttu-id="8af7d-135">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="8af7d-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="8af7d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8af7d-136">System.String</span></span>

## <span data-ttu-id="8af7d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8af7d-137">OUTPUTS</span></span>

### <span data-ttu-id="8af7d-138">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="8af7d-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="8af7d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8af7d-139">NOTES</span></span>

## <span data-ttu-id="8af7d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8af7d-140">RELATED LINKS</span></span>
