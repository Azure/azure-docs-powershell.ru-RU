---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078644"
---
# <span data-ttu-id="9533f-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9533f-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="9533f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9533f-102">SYNOPSIS</span></span>
<span data-ttu-id="9533f-103">Создание базы данных экземпляра SQL с управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="9533f-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="9533f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9533f-104">SYNTAX</span></span>

### <span data-ttu-id="9533f-105">CreateNewInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9533f-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9533f-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9533f-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9533f-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="9533f-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9533f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9533f-108">DESCRIPTION</span></span>
<span data-ttu-id="9533f-109">Командлет **New-AzSqlInstanceDatabase** создает базу данных экземпляра, управляемой с помощью Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9533f-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="9533f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9533f-110">EXAMPLES</span></span>

### <span data-ttu-id="9533f-111">Пример 1: создание базы данных на указанном экземпляре</span><span class="sxs-lookup"><span data-stu-id="9533f-111">Example 1: Create a database on a specified instance</span></span>
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

<span data-ttu-id="9533f-112">Эта команда создает базу данных экземпляра с именем Database01 на экземпляре managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="9533f-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="9533f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9533f-113">PARAMETERS</span></span>

### <span data-ttu-id="9533f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9533f-114">-AsJob</span></span>
<span data-ttu-id="9533f-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9533f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9533f-116">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="9533f-116">-Collation</span></span>
<span data-ttu-id="9533f-117">Параметры сортировки базы данных экземпляра SQL Azure для использования.</span><span class="sxs-lookup"><span data-stu-id="9533f-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="9533f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9533f-118">-DefaultProfile</span></span>
<span data-ttu-id="9533f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9533f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9533f-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9533f-120">-InstanceName</span></span>
<span data-ttu-id="9533f-121">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9533f-121">The instance name.</span></span>

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

### <span data-ttu-id="9533f-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="9533f-122">-InstanceObject</span></span>
<span data-ttu-id="9533f-123">Объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="9533f-123">The instance object</span></span>

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

### <span data-ttu-id="9533f-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="9533f-124">-InstanceResourceId</span></span>
<span data-ttu-id="9533f-125">Идентификатор ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="9533f-125">The instance resource id</span></span>

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

### <span data-ttu-id="9533f-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9533f-126">-Name</span></span>
<span data-ttu-id="9533f-127">Имя создаваемой базы данных экземпляра SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9533f-127">The name of the Azure SQL Instance Database to create.</span></span>

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

### <span data-ttu-id="9533f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9533f-128">-ResourceGroupName</span></span>
<span data-ttu-id="9533f-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9533f-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="9533f-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="9533f-130">-Tag</span></span>
<span data-ttu-id="9533f-131">Теги, связываемые с базой данных экземпляра Azure SQL</span><span class="sxs-lookup"><span data-stu-id="9533f-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="9533f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9533f-132">-Confirm</span></span>
<span data-ttu-id="9533f-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9533f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9533f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9533f-134">-WhatIf</span></span>
<span data-ttu-id="9533f-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9533f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9533f-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9533f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9533f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9533f-137">CommonParameters</span></span>
<span data-ttu-id="9533f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9533f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9533f-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9533f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9533f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9533f-140">INPUTS</span></span>

### <span data-ttu-id="9533f-141">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9533f-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="9533f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9533f-142">System.String</span></span>

## <span data-ttu-id="9533f-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9533f-143">OUTPUTS</span></span>

### <span data-ttu-id="9533f-144">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9533f-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9533f-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9533f-145">NOTES</span></span>

## <span data-ttu-id="9533f-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9533f-146">RELATED LINKS</span></span>
