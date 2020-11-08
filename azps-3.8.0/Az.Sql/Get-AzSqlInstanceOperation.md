---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: b9f008d610729d1f1bc73affbb5b8f3eae04ecdd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074259"
---
# <span data-ttu-id="97b2f-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="97b2f-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="97b2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="97b2f-103">Возвращает операции экземпляра, управляемого SQL.</span><span class="sxs-lookup"><span data-stu-id="97b2f-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="97b2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97b2f-104">SYNTAX</span></span>

### <span data-ttu-id="97b2f-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97b2f-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <Guid>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97b2f-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b2f-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97b2f-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="97b2f-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97b2f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97b2f-108">DESCRIPTION</span></span>
<span data-ttu-id="97b2f-109">Командлет Get-AzSqlInstanceOperation получает сведения об операциях в управляемом экземпляре SQL.</span><span class="sxs-lookup"><span data-stu-id="97b2f-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="97b2f-110">Вы можете просмотреть все операции на управляемом экземпляре или просмотреть определенную операцию, указав имя операции.</span><span class="sxs-lookup"><span data-stu-id="97b2f-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="97b2f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97b2f-111">EXAMPLES</span></span>

### <span data-ttu-id="97b2f-112">Пример 1: получение всех операций экземпляра</span><span class="sxs-lookup"><span data-stu-id="97b2f-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
```

<span data-ttu-id="97b2f-113">Эта команда возвращает все операции, управляемые экземпляром SQL.</span><span class="sxs-lookup"><span data-stu-id="97b2f-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="97b2f-114">Пример 2: получение определенной операции</span><span class="sxs-lookup"><span data-stu-id="97b2f-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
```

<span data-ttu-id="97b2f-115">Эта команда получает операцию с именем "5870c6d8-6703-4b27-8ae4-687b4ca7caea" в управляемом экземпляре SQL.</span><span class="sxs-lookup"><span data-stu-id="97b2f-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="97b2f-116">Пример 3: использование идентификатора ресурса операции</span><span class="sxs-lookup"><span data-stu-id="97b2f-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
```

<span data-ttu-id="97b2f-117">Эта команда получает операцию с идентификатором "/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea".</span><span class="sxs-lookup"><span data-stu-id="97b2f-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="97b2f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97b2f-118">PARAMETERS</span></span>

### <span data-ttu-id="97b2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b2f-119">-DefaultProfile</span></span>
<span data-ttu-id="97b2f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97b2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97b2f-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="97b2f-121">-ManagedInstanceName</span></span>
<span data-ttu-id="97b2f-122">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="97b2f-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b2f-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97b2f-123">-Name</span></span>
<span data-ttu-id="97b2f-124">Имя операции.</span><span class="sxs-lookup"><span data-stu-id="97b2f-124">The name of the operation.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b2f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b2f-125">-ResourceGroupName</span></span>
<span data-ttu-id="97b2f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97b2f-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b2f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97b2f-127">-ResourceId</span></span>
<span data-ttu-id="97b2f-128">Идентификатор ресурса операции управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="97b2f-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b2f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b2f-129">CommonParameters</span></span>
<span data-ttu-id="97b2f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97b2f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b2f-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97b2f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b2f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97b2f-132">INPUTS</span></span>

### <span data-ttu-id="97b2f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="97b2f-133">System.String</span></span>

## <span data-ttu-id="97b2f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97b2f-134">OUTPUTS</span></span>

### <span data-ttu-id="97b2f-135">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="97b2f-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="97b2f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="97b2f-136">NOTES</span></span>

## <span data-ttu-id="97b2f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97b2f-137">RELATED LINKS</span></span>
