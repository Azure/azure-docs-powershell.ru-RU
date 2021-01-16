---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 002dbbf0a5d244f992beb8a6591907a4c38ed6ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419471"
---
# <span data-ttu-id="d98f6-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="d98f6-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="d98f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d98f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d98f6-103">Включает проверку подлинности Azure AD только для определенного SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d98f6-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="d98f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d98f6-104">SYNTAX</span></span>

### <span data-ttu-id="d98f6-105">UseResourceGroupAndServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d98f6-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98f6-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d98f6-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98f6-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d98f6-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d98f6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d98f6-108">DESCRIPTION</span></span>
<span data-ttu-id="d98f6-109">Для **AzureSQlServerActiveDirectoryOnlyAuthentication** для Azure Active Directory (Azure AD) требуется проверка подлинности только для AzureSQL Server в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="d98f6-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="d98f6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d98f6-110">EXAMPLES</span></span>

### <span data-ttu-id="d98f6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d98f6-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="d98f6-112">Эта команда обеспечивает проверку подлинности Azure Active Directory (Azure AD) только для сервера AzureSQL Server01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d98f6-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d98f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d98f6-113">PARAMETERS</span></span>

### <span data-ttu-id="d98f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98f6-114">-DefaultProfile</span></span>
<span data-ttu-id="d98f6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d98f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d98f6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d98f6-116">-InputObject</span></span>
<span data-ttu-id="d98f6-117">Объект SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="d98f6-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d98f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d98f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="d98f6-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d98f6-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d98f6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d98f6-120">-ResourceId</span></span>
<span data-ttu-id="d98f6-121">ИД используемого экземпляра ресурса</span><span class="sxs-lookup"><span data-stu-id="d98f6-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="d98f6-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d98f6-122">-ServerName</span></span>
<span data-ttu-id="d98f6-123">Имя Azure SQL Server проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d98f6-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d98f6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d98f6-124">-Confirm</span></span>
<span data-ttu-id="d98f6-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d98f6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d98f6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d98f6-126">-WhatIf</span></span>
<span data-ttu-id="d98f6-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d98f6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d98f6-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d98f6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d98f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98f6-129">CommonParameters</span></span>
<span data-ttu-id="d98f6-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98f6-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d98f6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98f6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d98f6-132">INPUTS</span></span>

### <span data-ttu-id="d98f6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d98f6-133">System.String</span></span>

## <span data-ttu-id="d98f6-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d98f6-134">OUTPUTS</span></span>

### <span data-ttu-id="d98f6-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="d98f6-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="d98f6-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d98f6-136">NOTES</span></span>

## <span data-ttu-id="d98f6-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d98f6-137">RELATED LINKS</span></span>

[<span data-ttu-id="d98f6-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="d98f6-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="d98f6-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="d98f6-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="d98f6-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d98f6-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="d98f6-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d98f6-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="d98f6-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="d98f6-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)