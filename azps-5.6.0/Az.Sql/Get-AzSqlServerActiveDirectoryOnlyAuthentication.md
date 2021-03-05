---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 0b1759d6c2dc364904c50df010e6151351999f8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974200"
---
# <span data-ttu-id="8e5e2-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="8e5e2-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="8e5e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e5e2-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5e2-103">Получает проверку подлинности Azure AD только для определенного SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="8e5e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e5e2-104">SYNTAX</span></span>

### <span data-ttu-id="8e5e2-105">UseResourceGroupAndServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e5e2-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e5e2-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e5e2-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e5e2-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e5e2-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e5e2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e5e2-108">DESCRIPTION</span></span>
<span data-ttu-id="8e5e2-109">Для **azureSQLServerActiveDirectoryOnlyAuthentication** требуется только проверка подлинности Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8e5e2-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="8e5e2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e5e2-110">EXAMPLES</span></span>

### <span data-ttu-id="8e5e2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e5e2-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="8e5e2-112">Эта команда получает от Azure Active Directory (Azure AD) только требования к проверке подлинности для сервера AzureSQL Server01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8e5e2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e5e2-113">PARAMETERS</span></span>

### <span data-ttu-id="8e5e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5e2-114">-DefaultProfile</span></span>
<span data-ttu-id="8e5e2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e5e2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e5e2-116">-InputObject</span></span>
<span data-ttu-id="8e5e2-117">Объект SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="8e5e2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e5e2-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e5e2-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e5e2-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e5e2-120">-ResourceId</span></span>
<span data-ttu-id="8e5e2-121">ИД используемого экземпляра ресурса</span><span class="sxs-lookup"><span data-stu-id="8e5e2-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="8e5e2-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e5e2-122">-ServerName</span></span>
<span data-ttu-id="8e5e2-123">Имя Azure SQL Server проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="8e5e2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e5e2-124">-Confirm</span></span>
<span data-ttu-id="8e5e2-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e5e2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e5e2-126">-WhatIf</span></span>
<span data-ttu-id="8e5e2-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e5e2-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e5e2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5e2-129">CommonParameters</span></span>
<span data-ttu-id="8e5e2-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5e2-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e5e2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5e2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e5e2-132">INPUTS</span></span>

### <span data-ttu-id="8e5e2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8e5e2-133">System.String</span></span>

## <span data-ttu-id="8e5e2-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e5e2-134">OUTPUTS</span></span>

### <span data-ttu-id="8e5e2-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="8e5e2-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="8e5e2-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e5e2-136">NOTES</span></span>

## <span data-ttu-id="8e5e2-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e5e2-137">RELATED LINKS</span></span>

[<span data-ttu-id="8e5e2-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="8e5e2-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="8e5e2-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="8e5e2-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="8e5e2-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8e5e2-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8e5e2-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8e5e2-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="8e5e2-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="8e5e2-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)