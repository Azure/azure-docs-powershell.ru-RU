---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505866"
---
# <span data-ttu-id="44c2e-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="44c2e-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="44c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="44c2e-103">Удаляет базу данных azure SQL Управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="44c2e-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="44c2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="44c2e-104">SYNTAX</span></span>

### <span data-ttu-id="44c2e-105">RemoveInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44c2e-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c2e-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="44c2e-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c2e-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="44c2e-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44c2e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c2e-108">DESCRIPTION</span></span>
<span data-ttu-id="44c2e-109">Для удаления базы данных управляемого экземпляра Azure SQL удаляется SQL **AzSqlInstanceDatabase.**</span><span class="sxs-lookup"><span data-stu-id="44c2e-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="44c2e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="44c2e-110">EXAMPLES</span></span>

### <span data-ttu-id="44c2e-111">Пример 1. Удаление базы данных из экземпляра</span><span class="sxs-lookup"><span data-stu-id="44c2e-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="44c2e-112">Эта команда удаляет базу данных с именем Database01 из экземпляра ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="44c2e-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="44c2e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44c2e-113">PARAMETERS</span></span>

### <span data-ttu-id="44c2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c2e-114">-DefaultProfile</span></span>
<span data-ttu-id="44c2e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44c2e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c2e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="44c2e-116">-Force</span></span>
<span data-ttu-id="44c2e-117">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="44c2e-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="44c2e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44c2e-118">-InputObject</span></span>
<span data-ttu-id="44c2e-119">Удаляемый объект базы данных экземпляра</span><span class="sxs-lookup"><span data-stu-id="44c2e-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44c2e-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="44c2e-120">-InstanceName</span></span>
<span data-ttu-id="44c2e-121">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="44c2e-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c2e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="44c2e-122">-Name</span></span>
<span data-ttu-id="44c2e-123">Имя базы данных экземпляра Azure SQL для удаления.</span><span class="sxs-lookup"><span data-stu-id="44c2e-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44c2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="44c2e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44c2e-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c2e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44c2e-126">-ResourceId</span></span>
<span data-ttu-id="44c2e-127">ИД ресурса объекта базы данных экземпляра, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="44c2e-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c2e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44c2e-128">-Confirm</span></span>
<span data-ttu-id="44c2e-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="44c2e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c2e-130">-WhatIf</span></span>
<span data-ttu-id="44c2e-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44c2e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c2e-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="44c2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c2e-133">CommonParameters</span></span>
<span data-ttu-id="44c2e-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c2e-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44c2e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c2e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44c2e-136">INPUTS</span></span>

### <span data-ttu-id="44c2e-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="44c2e-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="44c2e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="44c2e-138">System.String</span></span>

## <span data-ttu-id="44c2e-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="44c2e-139">OUTPUTS</span></span>

### <span data-ttu-id="44c2e-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="44c2e-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="44c2e-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="44c2e-141">NOTES</span></span>

## <span data-ttu-id="44c2e-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44c2e-142">RELATED LINKS</span></span>
