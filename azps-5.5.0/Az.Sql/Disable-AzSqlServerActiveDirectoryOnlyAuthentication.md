---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 8d9214b44d5e408717968d042a1cdb86cd25130a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230260"
---
# <span data-ttu-id="6e580-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="6e580-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="6e580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e580-102">SYNOPSIS</span></span>
<span data-ttu-id="6e580-103">Отключает проверку подлинности Azure AD только для определенного SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e580-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="6e580-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e580-104">SYNTAX</span></span>

### <span data-ttu-id="6e580-105">UseResourceGroupAndServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e580-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e580-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e580-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e580-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e580-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e580-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e580-108">DESCRIPTION</span></span>
<span data-ttu-id="6e580-109">Для  AzureSQL Server, действующей в текущей подписке, для azureSQL Server отключена только проверка подлинности Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="6e580-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="6e580-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e580-110">EXAMPLES</span></span>

### <span data-ttu-id="6e580-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e580-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="6e580-112">Эта команда отключает только требования проверки подлинности Azure Active Directory (Azure AD) для сервера AzureSQL Server01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6e580-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="6e580-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e580-113">PARAMETERS</span></span>

### <span data-ttu-id="6e580-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e580-114">-DefaultProfile</span></span>
<span data-ttu-id="6e580-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e580-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e580-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e580-116">-InputObject</span></span>
<span data-ttu-id="6e580-117">Объект SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="6e580-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="6e580-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e580-118">-ResourceGroupName</span></span>
<span data-ttu-id="6e580-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e580-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e580-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e580-120">-ResourceId</span></span>
<span data-ttu-id="6e580-121">ИД используемого экземпляра ресурса</span><span class="sxs-lookup"><span data-stu-id="6e580-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="6e580-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e580-122">-ServerName</span></span>
<span data-ttu-id="6e580-123">Имя Azure SQL Server только для проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6e580-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="6e580-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e580-124">-Confirm</span></span>
<span data-ttu-id="6e580-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e580-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e580-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e580-126">-WhatIf</span></span>
<span data-ttu-id="6e580-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e580-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e580-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6e580-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e580-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e580-129">CommonParameters</span></span>
<span data-ttu-id="6e580-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e580-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e580-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e580-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e580-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e580-132">INPUTS</span></span>

### <span data-ttu-id="6e580-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6e580-133">System.String</span></span>

## <span data-ttu-id="6e580-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e580-134">OUTPUTS</span></span>

### <span data-ttu-id="6e580-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="6e580-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="6e580-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e580-136">NOTES</span></span>

## <span data-ttu-id="6e580-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e580-137">RELATED LINKS</span></span>

[<span data-ttu-id="6e580-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="6e580-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="6e580-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="6e580-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="6e580-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6e580-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="6e580-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6e580-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="6e580-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="6e580-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)