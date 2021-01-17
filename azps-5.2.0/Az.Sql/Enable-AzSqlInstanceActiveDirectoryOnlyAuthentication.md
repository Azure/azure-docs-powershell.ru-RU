---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392519"
---
# <span data-ttu-id="803db-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="803db-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="803db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="803db-102">SYNOPSIS</span></span>
<span data-ttu-id="803db-103">Включает проверку подлинности Azure AD только для определенного SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="803db-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="803db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="803db-104">SYNTAX</span></span>

### <span data-ttu-id="803db-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="803db-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="803db-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="803db-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="803db-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="803db-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="803db-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="803db-108">DESCRIPTION</span></span>
<span data-ttu-id="803db-109">С помощью **cmdletOnlyAuthentication Enable-AzSqlInstanceActiveDirectory** можно включить только требования проверки подлинности Azure Active Directory (Azure AD) для экземпляра AzureSQL, управляемого в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="803db-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="803db-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="803db-110">EXAMPLES</span></span>

### <span data-ttu-id="803db-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="803db-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="803db-112">Эта команда обеспечивает проверку подлинности Azure Active Directory (Azure AD) только для управляемого экземпляра AzureSQL ManagedInstance01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="803db-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="803db-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="803db-113">PARAMETERS</span></span>

### <span data-ttu-id="803db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803db-114">-DefaultProfile</span></span>
<span data-ttu-id="803db-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="803db-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="803db-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="803db-116">-InputObject</span></span>
<span data-ttu-id="803db-117">Объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="803db-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="803db-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="803db-118">-InstanceName</span></span>
<span data-ttu-id="803db-119">Имя управляемого экземпляра Azure SQL только для проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="803db-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="803db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="803db-120">-ResourceGroupName</span></span>
<span data-ttu-id="803db-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="803db-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="803db-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="803db-122">-ResourceId</span></span>
<span data-ttu-id="803db-123">ИД используемого экземпляра ресурса</span><span class="sxs-lookup"><span data-stu-id="803db-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="803db-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="803db-124">-Confirm</span></span>
<span data-ttu-id="803db-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="803db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="803db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="803db-126">-WhatIf</span></span>
<span data-ttu-id="803db-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="803db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="803db-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="803db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="803db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803db-129">CommonParameters</span></span>
<span data-ttu-id="803db-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="803db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803db-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="803db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803db-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="803db-132">INPUTS</span></span>

### <span data-ttu-id="803db-133">System.String</span><span class="sxs-lookup"><span data-stu-id="803db-133">System.String</span></span>

## <span data-ttu-id="803db-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="803db-134">OUTPUTS</span></span>

### <span data-ttu-id="803db-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="803db-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="803db-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="803db-136">NOTES</span></span>

## <span data-ttu-id="803db-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="803db-137">RELATED LINKS</span></span>

[<span data-ttu-id="803db-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="803db-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="803db-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="803db-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="803db-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="803db-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="803db-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="803db-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)