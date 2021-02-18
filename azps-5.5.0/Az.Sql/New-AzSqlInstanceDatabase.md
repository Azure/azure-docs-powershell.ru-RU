---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231772"
---
# <span data-ttu-id="dae7c-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dae7c-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="dae7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dae7c-102">SYNOPSIS</span></span>
<span data-ttu-id="dae7c-103">Создает базу данных azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="dae7c-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="dae7c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dae7c-104">SYNTAX</span></span>

### <span data-ttu-id="dae7c-105">CreateNewInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dae7c-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae7c-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="dae7c-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae7c-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="dae7c-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dae7c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dae7c-108">DESCRIPTION</span></span>
<span data-ttu-id="dae7c-109">Для создания базы данных управляемого экземпляра Azure SQL **AzSqlInstanceDatabase.**</span><span class="sxs-lookup"><span data-stu-id="dae7c-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="dae7c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dae7c-110">EXAMPLES</span></span>

### <span data-ttu-id="dae7c-111">Пример 1. Создание базы данных в указанном экземпляре</span><span class="sxs-lookup"><span data-stu-id="dae7c-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="dae7c-112">Эта команда создает базу данных экземпляра Database01 для экземпляра ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="dae7c-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="dae7c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dae7c-113">PARAMETERS</span></span>

### <span data-ttu-id="dae7c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dae7c-114">-AsJob</span></span>
<span data-ttu-id="dae7c-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dae7c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dae7c-116">-Collation</span><span class="sxs-lookup"><span data-stu-id="dae7c-116">-Collation</span></span>
<span data-ttu-id="dae7c-117">Разлиновка разной разлиновки SQL экземпляра базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dae7c-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae7c-118">-DefaultProfile</span></span>
<span data-ttu-id="dae7c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dae7c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dae7c-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="dae7c-120">-InstanceName</span></span>
<span data-ttu-id="dae7c-121">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dae7c-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae7c-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="dae7c-122">-InstanceObject</span></span>
<span data-ttu-id="dae7c-123">Объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="dae7c-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dae7c-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="dae7c-124">-InstanceResourceId</span></span>
<span data-ttu-id="dae7c-125">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="dae7c-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae7c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="dae7c-126">-Name</span></span>
<span data-ttu-id="dae7c-127">Имя создаемой базы SQL Экземпляр Azure.</span><span class="sxs-lookup"><span data-stu-id="dae7c-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae7c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae7c-128">-ResourceGroupName</span></span>
<span data-ttu-id="dae7c-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dae7c-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae7c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="dae7c-130">-Tag</span></span>
<span data-ttu-id="dae7c-131">Теги, которые нужно связать с базой данных экземпляра Azure Sql</span><span class="sxs-lookup"><span data-stu-id="dae7c-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dae7c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dae7c-132">-Confirm</span></span>
<span data-ttu-id="dae7c-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dae7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae7c-134">-WhatIf</span></span>
<span data-ttu-id="dae7c-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dae7c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dae7c-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dae7c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae7c-137">CommonParameters</span></span>
<span data-ttu-id="dae7c-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae7c-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dae7c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae7c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dae7c-140">INPUTS</span></span>

### <span data-ttu-id="dae7c-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="dae7c-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="dae7c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dae7c-142">System.String</span></span>

## <span data-ttu-id="dae7c-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dae7c-143">OUTPUTS</span></span>

### <span data-ttu-id="dae7c-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="dae7c-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="dae7c-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dae7c-145">NOTES</span></span>

## <span data-ttu-id="dae7c-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dae7c-146">RELATED LINKS</span></span>
