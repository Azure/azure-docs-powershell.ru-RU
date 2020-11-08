---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235763"
---
# <span data-ttu-id="e8f8c-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8f8c-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e8f8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f8c-103">Подготовка экземпляра Azure AD к управляемому экземпляру SQL.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="e8f8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8f8c-104">SYNTAX</span></span>

### <span data-ttu-id="e8f8c-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8f8c-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f8c-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8f8c-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8f8c-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8f8c-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f8c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f8c-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f8c-109">Командлет **Set-AzSqlInstanceActiveDirectoryAdministrator** подготавливает администратора Azure Active Directory (Azure AD) для AzureSQL управляемого экземпляра в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="e8f8c-110">Вы можете подготовить только одного администратора за один раз.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="e8f8c-111">Следующие участники Azure AD могут быть предоставлены в качестве администратора SQL для управляемых экземпляров:</span><span class="sxs-lookup"><span data-stu-id="e8f8c-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="e8f8c-112">Собственные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="e8f8c-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="e8f8c-113">Федеративные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="e8f8c-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="e8f8c-114">Группы Azure AD, созданные как группы безопасности, импортированные из других рекламных объявлений Azure, не поддерживаются как администраторы.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="e8f8c-115">Учетные записи Майкрософт, например, в доменах Outlook.com, Hotmail.com или Live.com, не поддерживаются в качестве администраторов.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="e8f8c-116">Другие гостевые учетные записи, например в доменах Gmail.com и Yahoo.com, не поддерживаются в качестве администраторов.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="e8f8c-117">Рекомендуем предоставить специальную группу Azure AD в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="e8f8c-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8f8c-118">EXAMPLES</span></span>

### <span data-ttu-id="e8f8c-119">Пример 1: подготовка группы администраторов для управляемого экземпляра, связанного с группой ресурсов</span><span class="sxs-lookup"><span data-stu-id="e8f8c-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e8f8c-120">Эта команда подготавливает группу администраторов Azure Active Directory с именем "Администраторы доменных имен" для управляемого экземпляра с именем ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="e8f8c-121">Этот сервер связан с группой ResourceGroup01 ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="e8f8c-122">Пример 2: подготовка пользователя администратора с помощью объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="e8f8c-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="e8f8c-123">Эта команда подготавливает пользователя Azure AD к учетной записи администратора из объекта управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="e8f8c-124">Пример 3: подготовка администратора с помощью идентификатора ресурса управляемых экземпляров</span><span class="sxs-lookup"><span data-stu-id="e8f8c-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="e8f8c-125">Эта команда предоставляет пользователю Azure AD роль администратора с помощью идентификатора ресурса управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="e8f8c-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8f8c-126">PARAMETERS</span></span>

### <span data-ttu-id="e8f8c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f8c-127">-DefaultProfile</span></span>
<span data-ttu-id="e8f8c-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f8c-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e8f8c-129">-DisplayName</span></span>
<span data-ttu-id="e8f8c-130">Указывает отображаемое имя пользователя или группы, которым нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="e8f8c-131">Это отображаемое имя должно существовать в службе каталогов Active Directory, связанной с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8f8c-132">-InputObject</span></span>
<span data-ttu-id="e8f8c-133">Используемый объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8c-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e8f8c-134">-InstanceName</span></span>
<span data-ttu-id="e8f8c-135">Имя экземпляра с управляемым SQL.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-135">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8c-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e8f8c-136">-ObjectId</span></span>
<span data-ttu-id="e8f8c-137">Указывает идентификатор объекта пользователя или группы в Azure Active Directory, для которого требуется предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f8c-138">-ResourceGroupName</span></span>
<span data-ttu-id="e8f8c-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8c-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f8c-140">-ResourceId</span></span>
<span data-ttu-id="e8f8c-141">Идентификатор ресурса используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-141">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f8c-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8f8c-142">-Confirm</span></span>
<span data-ttu-id="e8f8c-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f8c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f8c-144">-WhatIf</span></span>
<span data-ttu-id="e8f8c-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f8c-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f8c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f8c-147">CommonParameters</span></span>
<span data-ttu-id="e8f8c-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8f8c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f8c-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8f8c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f8c-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8f8c-150">INPUTS</span></span>

### <span data-ttu-id="e8f8c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f8c-151">System.String</span></span>

### <span data-ttu-id="e8f8c-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e8f8c-152">System.Guid</span></span>

## <span data-ttu-id="e8f8c-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f8c-153">OUTPUTS</span></span>

### <span data-ttu-id="e8f8c-154">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e8f8c-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e8f8c-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8f8c-155">NOTES</span></span>

## <span data-ttu-id="e8f8c-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8f8c-156">RELATED LINKS</span></span>

[<span data-ttu-id="e8f8c-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8f8c-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="e8f8c-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e8f8c-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
