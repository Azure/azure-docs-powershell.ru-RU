---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230052"
---
# <span data-ttu-id="9a44c-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="9a44c-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="9a44c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a44c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a44c-103">Удаляет виртуальный кластер Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9a44c-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="9a44c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a44c-104">SYNTAX</span></span>

### <span data-ttu-id="9a44c-105">RemoveVirtualClusterFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a44c-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a44c-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="9a44c-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a44c-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="9a44c-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a44c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a44c-108">DESCRIPTION</span></span>
<span data-ttu-id="9a44c-109">При этом из виртуального кластера Azure SQL удаляется SQL **AzSqlVirtualCluster.**</span><span class="sxs-lookup"><span data-stu-id="9a44c-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="9a44c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a44c-110">EXAMPLES</span></span>

### <span data-ttu-id="9a44c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a44c-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="9a44c-112">Эта команда удаляет виртуальный кластер VirtualCluster1, который назначен группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9a44c-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="9a44c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a44c-113">PARAMETERS</span></span>

### <span data-ttu-id="9a44c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a44c-114">-AsJob</span></span>
<span data-ttu-id="9a44c-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9a44c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a44c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a44c-116">-DefaultProfile</span></span>
<span data-ttu-id="9a44c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a44c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a44c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a44c-118">-InputObject</span></span>
<span data-ttu-id="9a44c-119">Удаляемый объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="9a44c-119">The instance object to remove</span></span>

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

### <span data-ttu-id="9a44c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9a44c-120">-Name</span></span>
<span data-ttu-id="9a44c-121">Имя виртуального кластера.</span><span class="sxs-lookup"><span data-stu-id="9a44c-121">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="9a44c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a44c-122">-ResourceGroupName</span></span>
<span data-ttu-id="9a44c-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a44c-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a44c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a44c-124">-ResourceId</span></span>
<span data-ttu-id="9a44c-125">ИД ресурса объекта экземпляра, который требуется удалить</span><span class="sxs-lookup"><span data-stu-id="9a44c-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="9a44c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a44c-126">-Confirm</span></span>
<span data-ttu-id="9a44c-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9a44c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a44c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a44c-128">-WhatIf</span></span>
<span data-ttu-id="9a44c-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a44c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a44c-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a44c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a44c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a44c-131">CommonParameters</span></span>
<span data-ttu-id="9a44c-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a44c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a44c-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a44c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a44c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a44c-134">INPUTS</span></span>

### <span data-ttu-id="9a44c-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="9a44c-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="9a44c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9a44c-136">System.String</span></span>

## <span data-ttu-id="9a44c-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a44c-137">OUTPUTS</span></span>

### <span data-ttu-id="9a44c-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="9a44c-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="9a44c-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a44c-139">NOTES</span></span>

## <span data-ttu-id="9a44c-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a44c-140">RELATED LINKS</span></span>
