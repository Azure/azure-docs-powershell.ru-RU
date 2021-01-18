---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506457"
---
# <span data-ttu-id="e66c0-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e66c0-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e66c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e66c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e66c0-103">Подготовка администратора Azure AD для SQL управляемым экземпляром.</span><span class="sxs-lookup"><span data-stu-id="e66c0-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="e66c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e66c0-104">SYNTAX</span></span>

### <span data-ttu-id="e66c0-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e66c0-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e66c0-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e66c0-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e66c0-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e66c0-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e66c0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e66c0-108">DESCRIPTION</span></span>
<span data-ttu-id="e66c0-109">Для управляемого экземпляра AzureSQL в текущей подписке для администратора **Set-AzSqlInstanceActiveDirectoryAdministrator** предусмотрен администратор Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e66c0-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="e66c0-110">Одновременно можно подготовка только одного администратора.</span><span class="sxs-lookup"><span data-stu-id="e66c0-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="e66c0-111">Следующими участниками Azure AD могут быть предусмотрены права администратора SQL управляемых экземпляров:</span><span class="sxs-lookup"><span data-stu-id="e66c0-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="e66c0-112">Участники, которые являются участниками Azure AD</span><span class="sxs-lookup"><span data-stu-id="e66c0-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="e66c0-113">Федераированные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="e66c0-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="e66c0-114">Группы Azure AD, созданные как группы безопасности, импортируемые из других служб Azure ADs, не поддерживаются администраторами.</span><span class="sxs-lookup"><span data-stu-id="e66c0-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="e66c0-115">Учетные записи Майкрософт, например учетные записи Outlook.com, Hotmail.com или Live.com, не поддерживаются администраторами.</span><span class="sxs-lookup"><span data-stu-id="e66c0-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="e66c0-116">Другие гостевых учетные записи, например учетные записи Gmail.com или Yahoo.com, не поддерживаются администраторами.</span><span class="sxs-lookup"><span data-stu-id="e66c0-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="e66c0-117">Мы рекомендуем на правах администратора использовать специальную группу Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e66c0-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="e66c0-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e66c0-118">EXAMPLES</span></span>

### <span data-ttu-id="e66c0-119">Пример 1. Подготовка группы администраторов для управляемого экземпляра, связанного с группой ресурсов</span><span class="sxs-lookup"><span data-stu-id="e66c0-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e66c0-120">Эта команда предусматривает группу администраторов Azure AD с именем DBAs для управляемого экземпляра ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="e66c0-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="e66c0-121">Этот сервер связан с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e66c0-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="e66c0-122">Пример 2. Подготовка пользователя администратора с помощью управляемого объекта экземпляра</span><span class="sxs-lookup"><span data-stu-id="e66c0-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="e66c0-123">Эта команда предусматривает предоставление пользователя Azure AD в качестве администратора для объекта управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e66c0-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="e66c0-124">Пример 3. Подготовка администратора с помощью идентификатора ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="e66c0-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="e66c0-125">Эта команда позволяет пользователю Azure AD стать администратором с помощью идентификатора ресурса управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e66c0-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="e66c0-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e66c0-126">PARAMETERS</span></span>

### <span data-ttu-id="e66c0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e66c0-127">-DefaultProfile</span></span>
<span data-ttu-id="e66c0-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e66c0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e66c0-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e66c0-129">-DisplayName</span></span>
<span data-ttu-id="e66c0-130">Отображает имя пользователя или группы, для которых нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="e66c0-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="e66c0-131">Это отображаемая имя должна существовать в активном каталоге, связанном с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="e66c0-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="e66c0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e66c0-132">-InputObject</span></span>
<span data-ttu-id="e66c0-133">Объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e66c0-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="e66c0-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e66c0-134">-InstanceName</span></span>
<span data-ttu-id="e66c0-135">SQL управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e66c0-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="e66c0-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e66c0-136">-ObjectId</span></span>
<span data-ttu-id="e66c0-137">Определяет ИД объекта пользователя или группы в Azure Active Directory, для которого нужно предоставить разрешения.</span><span class="sxs-lookup"><span data-stu-id="e66c0-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="e66c0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e66c0-138">-ResourceGroupName</span></span>
<span data-ttu-id="e66c0-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e66c0-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="e66c0-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e66c0-140">-ResourceId</span></span>
<span data-ttu-id="e66c0-141">ИД используемого экземпляра ресурса</span><span class="sxs-lookup"><span data-stu-id="e66c0-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="e66c0-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e66c0-142">-Confirm</span></span>
<span data-ttu-id="e66c0-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e66c0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e66c0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e66c0-144">-WhatIf</span></span>
<span data-ttu-id="e66c0-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e66c0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e66c0-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e66c0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e66c0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e66c0-147">CommonParameters</span></span>
<span data-ttu-id="e66c0-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e66c0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e66c0-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e66c0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e66c0-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e66c0-150">INPUTS</span></span>

### <span data-ttu-id="e66c0-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e66c0-151">System.String</span></span>

### <span data-ttu-id="e66c0-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e66c0-152">System.Guid</span></span>

## <span data-ttu-id="e66c0-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e66c0-153">OUTPUTS</span></span>

### <span data-ttu-id="e66c0-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e66c0-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e66c0-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e66c0-155">NOTES</span></span>

## <span data-ttu-id="e66c0-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e66c0-156">RELATED LINKS</span></span>

[<span data-ttu-id="e66c0-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e66c0-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="e66c0-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e66c0-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
