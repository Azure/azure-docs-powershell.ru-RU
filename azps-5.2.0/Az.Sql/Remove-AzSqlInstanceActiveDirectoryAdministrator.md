---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416287"
---
# <span data-ttu-id="b6c4b-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b6c4b-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b6c4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c4b-103">Удаление администратора Azure AD для SQL управляемым экземпляром.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="b6c4b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6c4b-104">SYNTAX</span></span>

### <span data-ttu-id="b6c4b-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6c4b-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6c4b-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6c4b-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6c4b-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6c4b-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6c4b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6c4b-108">DESCRIPTION</span></span>
<span data-ttu-id="b6c4b-109">При наступлении cmdlet **Remove-AzSqlInstanceActiveDirectoryAdministrator** удаляется администратор Azure Active Directory (Azure AD) для управляемого экземпляра AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="b6c4b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6c4b-110">EXAMPLES</span></span>

### <span data-ttu-id="b6c4b-111">Пример 1. Удаление администратора</span><span class="sxs-lookup"><span data-stu-id="b6c4b-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b6c4b-112">Эта команда удаляет администратор Azure AD для управляемого экземпляра ManagedInstanceName01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="b6c4b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b6c4b-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b6c4b-114">Эта команда удаляет администратор Azure AD из объекта управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="b6c4b-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b6c4b-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="b6c4b-116">Эта команда удаляет администратор Azure AD с помощью идентификатора ресурса управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="b6c4b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6c4b-117">PARAMETERS</span></span>

### <span data-ttu-id="b6c4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c4b-118">-DefaultProfile</span></span>
<span data-ttu-id="b6c4b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6c4b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b6c4b-120">-Force</span></span>
<span data-ttu-id="b6c4b-121">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="b6c4b-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b6c4b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6c4b-122">-InputObject</span></span>
<span data-ttu-id="b6c4b-123">Объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="b6c4b-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b6c4b-124">-InstanceName</span></span>
<span data-ttu-id="b6c4b-125">SQL управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="b6c4b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6c4b-126">-PassThru</span></span>
<span data-ttu-id="b6c4b-127">Определяет, нужно ли вернуть удаленного администратора AD.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="b6c4b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6c4b-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6c4b-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="b6c4b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c4b-130">-ResourceId</span></span>
<span data-ttu-id="b6c4b-131">ИД используемого экземпляра ресурса</span><span class="sxs-lookup"><span data-stu-id="b6c4b-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="b6c4b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6c4b-132">-Confirm</span></span>
<span data-ttu-id="b6c4b-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c4b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c4b-134">-WhatIf</span></span>
<span data-ttu-id="b6c4b-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6c4b-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c4b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c4b-137">CommonParameters</span></span>
<span data-ttu-id="b6c4b-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c4b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c4b-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6c4b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c4b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6c4b-140">INPUTS</span></span>

### <span data-ttu-id="b6c4b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b6c4b-141">System.String</span></span>

## <span data-ttu-id="b6c4b-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6c4b-142">OUTPUTS</span></span>

### <span data-ttu-id="b6c4b-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="b6c4b-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="b6c4b-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6c4b-144">NOTES</span></span>

## <span data-ttu-id="b6c4b-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6c4b-145">RELATED LINKS</span></span>

[<span data-ttu-id="b6c4b-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b6c4b-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="b6c4b-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b6c4b-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
