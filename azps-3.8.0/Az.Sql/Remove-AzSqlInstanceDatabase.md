---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072809"
---
# <span data-ttu-id="43bd8-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="43bd8-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="43bd8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="43bd8-103">Удаляет базу данных экземпляра SQL, управляемую с помощью Azure.</span><span class="sxs-lookup"><span data-stu-id="43bd8-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="43bd8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43bd8-104">SYNTAX</span></span>

### <span data-ttu-id="43bd8-105">RemoveInstanceDatabaseFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43bd8-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43bd8-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="43bd8-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43bd8-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="43bd8-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43bd8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43bd8-108">DESCRIPTION</span></span>
<span data-ttu-id="43bd8-109">Командлет **Remove-AzSqlInstanceDatabase** удаляет базу данных экземпляра SQL с управляемой службой Azure.</span><span class="sxs-lookup"><span data-stu-id="43bd8-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="43bd8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43bd8-110">EXAMPLES</span></span>

### <span data-ttu-id="43bd8-111">Пример 1: Удаление базы данных из экземпляра</span><span class="sxs-lookup"><span data-stu-id="43bd8-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="43bd8-112">Эта команда удаляет базу данных с именем Database01 из экземпляра managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="43bd8-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="43bd8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43bd8-113">PARAMETERS</span></span>

### <span data-ttu-id="43bd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43bd8-114">-DefaultProfile</span></span>
<span data-ttu-id="43bd8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43bd8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43bd8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="43bd8-116">-Force</span></span>
<span data-ttu-id="43bd8-117">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="43bd8-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="43bd8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43bd8-118">-InputObject</span></span>
<span data-ttu-id="43bd8-119">Объект базы данных экземпляра, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="43bd8-119">The Instance Database object to remove</span></span>

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

### <span data-ttu-id="43bd8-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="43bd8-120">-InstanceName</span></span>
<span data-ttu-id="43bd8-121">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="43bd8-121">The instance name.</span></span>

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

### <span data-ttu-id="43bd8-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43bd8-122">-Name</span></span>
<span data-ttu-id="43bd8-123">Имя удаляемой базы данных экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="43bd8-123">The name of the Azure SQL Instance Database to remove.</span></span>

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

### <span data-ttu-id="43bd8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43bd8-124">-ResourceGroupName</span></span>
<span data-ttu-id="43bd8-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43bd8-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="43bd8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43bd8-126">-ResourceId</span></span>
<span data-ttu-id="43bd8-127">Идентификатор ресурса объекта базы данных экземпляра, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="43bd8-127">The resource id of Instance Database object to remove</span></span>

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

### <span data-ttu-id="43bd8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43bd8-128">-Confirm</span></span>
<span data-ttu-id="43bd8-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43bd8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43bd8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43bd8-130">-WhatIf</span></span>
<span data-ttu-id="43bd8-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43bd8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43bd8-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43bd8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43bd8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43bd8-133">CommonParameters</span></span>
<span data-ttu-id="43bd8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43bd8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43bd8-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43bd8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43bd8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43bd8-136">INPUTS</span></span>

### <span data-ttu-id="43bd8-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="43bd8-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="43bd8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="43bd8-138">System.String</span></span>

## <span data-ttu-id="43bd8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43bd8-139">OUTPUTS</span></span>

### <span data-ttu-id="43bd8-140">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="43bd8-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="43bd8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="43bd8-141">NOTES</span></span>

## <span data-ttu-id="43bd8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43bd8-142">RELATED LINKS</span></span>
