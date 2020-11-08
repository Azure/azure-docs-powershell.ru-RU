---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 002dbbf0a5d244f992beb8a6591907a4c38ed6ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235310"
---
# <span data-ttu-id="3193f-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3193f-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="3193f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3193f-102">SYNOPSIS</span></span>
<span data-ttu-id="3193f-103">Обеспечивается проверка подлинности в Azure AD для определенного сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3193f-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="3193f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3193f-104">SYNTAX</span></span>

### <span data-ttu-id="3193f-105">UseResourceGroupAndServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3193f-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3193f-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3193f-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3193f-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3193f-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3193f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3193f-108">DESCRIPTION</span></span>
<span data-ttu-id="3193f-109">Командлет **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** используется для использования Azure Active Directory (Azure AD) только для проверки подлинности для сервера AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="3193f-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="3193f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3193f-110">EXAMPLES</span></span>

### <span data-ttu-id="3193f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3193f-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="3193f-112">Эта команда активизирует Azure Active Directory (Azure AD) только требованием проверки подлинности для сервера AzureSQL с именем Server01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3193f-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3193f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3193f-113">PARAMETERS</span></span>

### <span data-ttu-id="3193f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3193f-114">-DefaultProfile</span></span>
<span data-ttu-id="3193f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3193f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3193f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3193f-116">-InputObject</span></span>
<span data-ttu-id="3193f-117">Используемый объект SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3193f-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="3193f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3193f-118">-ResourceGroupName</span></span>
<span data-ttu-id="3193f-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3193f-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="3193f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3193f-120">-ResourceId</span></span>
<span data-ttu-id="3193f-121">Идентификатор ресурса используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3193f-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="3193f-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3193f-122">-ServerName</span></span>
<span data-ttu-id="3193f-123">Имя сервера Azure SQL Server, в котором находится проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3193f-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="3193f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3193f-124">-Confirm</span></span>
<span data-ttu-id="3193f-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3193f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3193f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3193f-126">-WhatIf</span></span>
<span data-ttu-id="3193f-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3193f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3193f-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3193f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3193f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3193f-129">CommonParameters</span></span>
<span data-ttu-id="3193f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3193f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3193f-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3193f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3193f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3193f-132">INPUTS</span></span>

### <span data-ttu-id="3193f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3193f-133">System.String</span></span>

## <span data-ttu-id="3193f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3193f-134">OUTPUTS</span></span>

### <span data-ttu-id="3193f-135">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="3193f-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="3193f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3193f-136">NOTES</span></span>

## <span data-ttu-id="3193f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3193f-137">RELATED LINKS</span></span>

[<span data-ttu-id="3193f-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3193f-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3193f-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3193f-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3193f-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3193f-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3193f-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3193f-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3193f-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3193f-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)