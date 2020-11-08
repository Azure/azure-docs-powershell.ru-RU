---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: e5460fcbc48d36dab6309891247315f0539ff7ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246687"
---
# <span data-ttu-id="ff6bc-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ff6bc-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="ff6bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6bc-103">Получает только Azure AD Authentication для определенного сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="ff6bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff6bc-104">SYNTAX</span></span>

### <span data-ttu-id="ff6bc-105">UseResourceGroupAndServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff6bc-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6bc-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff6bc-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6bc-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff6bc-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff6bc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff6bc-108">DESCRIPTION</span></span>
<span data-ttu-id="ff6bc-109">Командлет **Get-AzSqlServerActiveDirectoryOnlyAuthentication** получает требование проверки подлинности для службы Azure Active Directory (Azure AD) только для сервера AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="ff6bc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff6bc-110">EXAMPLES</span></span>

### <span data-ttu-id="ff6bc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff6bc-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="ff6bc-112">Эта команда возвращает Azure Active Directory (Azure AD) только требование проверки подлинности для сервера AzureSQL с именем Server01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ff6bc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff6bc-113">PARAMETERS</span></span>

### <span data-ttu-id="ff6bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6bc-114">-DefaultProfile</span></span>
<span data-ttu-id="ff6bc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff6bc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff6bc-116">-InputObject</span></span>
<span data-ttu-id="ff6bc-117">Используемый объект SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="ff6bc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff6bc-118">-ResourceGroupName</span></span>
<span data-ttu-id="ff6bc-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff6bc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff6bc-120">-ResourceId</span></span>
<span data-ttu-id="ff6bc-121">Идентификатор ресурса используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="ff6bc-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ff6bc-122">-ServerName</span></span>
<span data-ttu-id="ff6bc-123">Имя сервера Azure SQL Server, в котором находится проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="ff6bc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff6bc-124">-Confirm</span></span>
<span data-ttu-id="ff6bc-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff6bc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff6bc-126">-WhatIf</span></span>
<span data-ttu-id="ff6bc-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff6bc-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff6bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6bc-129">CommonParameters</span></span>
<span data-ttu-id="ff6bc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff6bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6bc-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff6bc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6bc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff6bc-132">INPUTS</span></span>

### <span data-ttu-id="ff6bc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ff6bc-133">System.String</span></span>

## <span data-ttu-id="ff6bc-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff6bc-134">OUTPUTS</span></span>

### <span data-ttu-id="ff6bc-135">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="ff6bc-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="ff6bc-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff6bc-136">NOTES</span></span>

## <span data-ttu-id="ff6bc-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff6bc-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff6bc-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ff6bc-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ff6bc-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ff6bc-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ff6bc-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ff6bc-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ff6bc-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ff6bc-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ff6bc-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="ff6bc-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)