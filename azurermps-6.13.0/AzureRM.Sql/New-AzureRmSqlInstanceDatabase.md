---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 2ef6ff642d22429ae22186ce01a4a17dad125b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565331"
---
# <span data-ttu-id="d770b-101">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d770b-101">New-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="d770b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d770b-102">SYNOPSIS</span></span>
<span data-ttu-id="d770b-103">Создание базы данных экземпляра SQL с управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="d770b-103">Creates an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d770b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d770b-104">SYNTAX</span></span>

### <span data-ttu-id="d770b-105">CreateNewInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d770b-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d770b-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d770b-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d770b-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d770b-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d770b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d770b-108">DESCRIPTION</span></span>
<span data-ttu-id="d770b-109">Командлет **New-AzureRmSqlInstanceDatabase** создает базу данных экземпляра, управляемой с помощью Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d770b-109">The **New-AzureRmSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="d770b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d770b-110">EXAMPLES</span></span>

### <span data-ttu-id="d770b-111">Пример 1: создание базы данных на указанном экземпляре</span><span class="sxs-lookup"><span data-stu-id="d770b-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="d770b-112">Эта команда создает базу данных экземпляра с именем Database01 на экземпляре managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="d770b-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="d770b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d770b-113">PARAMETERS</span></span>

### <span data-ttu-id="d770b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d770b-114">-AsJob</span></span>
<span data-ttu-id="d770b-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d770b-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-116">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="d770b-116">-Collation</span></span>
<span data-ttu-id="d770b-117">Параметры сортировки базы данных экземпляра SQL Azure для использования.</span><span class="sxs-lookup"><span data-stu-id="d770b-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d770b-118">-DefaultProfile</span></span>
<span data-ttu-id="d770b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d770b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d770b-120">-InstanceName</span></span>
<span data-ttu-id="d770b-121">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d770b-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="d770b-122">-InstanceObject</span></span>
<span data-ttu-id="d770b-123">Объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="d770b-123">The instance object</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d770b-124">-InstanceResourceId</span></span>
<span data-ttu-id="d770b-125">Идентификатор ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="d770b-125">The instance resource id</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d770b-126">-Name</span></span>
<span data-ttu-id="d770b-127">Имя создаваемой базы данных экземпляра SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d770b-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d770b-128">-ResourceGroupName</span></span>
<span data-ttu-id="d770b-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d770b-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="d770b-130">-Tag</span></span>
<span data-ttu-id="d770b-131">Теги, связываемые с базой данных экземпляра Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d770b-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d770b-132">-Confirm</span></span>
<span data-ttu-id="d770b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d770b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d770b-134">-WhatIf</span></span>
<span data-ttu-id="d770b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d770b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d770b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d770b-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d770b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d770b-137">CommonParameters</span></span>
<span data-ttu-id="d770b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d770b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d770b-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d770b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d770b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d770b-140">INPUTS</span></span>

### <span data-ttu-id="d770b-141">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d770b-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="d770b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d770b-142">System.String</span></span>

## <span data-ttu-id="d770b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d770b-143">OUTPUTS</span></span>

### <span data-ttu-id="d770b-144">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d770b-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d770b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d770b-145">NOTES</span></span>

## <span data-ttu-id="d770b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d770b-146">RELATED LINKS</span></span>
