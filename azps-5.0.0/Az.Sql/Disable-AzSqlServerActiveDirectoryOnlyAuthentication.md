---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 8d9214b44d5e408717968d042a1cdb86cd25130a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245677"
---
# <span data-ttu-id="a2512-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a2512-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="a2512-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2512-102">SYNOPSIS</span></span>
<span data-ttu-id="a2512-103">Отключение проверки подлинности Azure AD для определенного сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2512-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="a2512-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2512-104">SYNTAX</span></span>

### <span data-ttu-id="a2512-105">UseResourceGroupAndServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2512-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2512-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2512-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2512-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2512-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2512-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2512-108">DESCRIPTION</span></span>
<span data-ttu-id="a2512-109">Командлет **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** отключает Azure Active Directory (Azure AD) только требованием проверки подлинности для сервера AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a2512-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="a2512-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2512-110">EXAMPLES</span></span>

### <span data-ttu-id="a2512-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2512-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="a2512-112">Эта команда отключает Azure Active Directory (Azure AD) только требованием проверки подлинности для сервера AzureSQL с именем Server01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a2512-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a2512-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2512-113">PARAMETERS</span></span>

### <span data-ttu-id="a2512-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2512-114">-DefaultProfile</span></span>
<span data-ttu-id="a2512-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2512-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2512-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2512-116">-InputObject</span></span>
<span data-ttu-id="a2512-117">Используемый объект SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2512-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="a2512-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2512-118">-ResourceGroupName</span></span>
<span data-ttu-id="a2512-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2512-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2512-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2512-120">-ResourceId</span></span>
<span data-ttu-id="a2512-121">Идентификатор ресурса используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a2512-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="a2512-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a2512-122">-ServerName</span></span>
<span data-ttu-id="a2512-123">Имя сервера Azure SQL Server, в котором находится проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2512-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="a2512-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2512-124">-Confirm</span></span>
<span data-ttu-id="a2512-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2512-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2512-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2512-126">-WhatIf</span></span>
<span data-ttu-id="a2512-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2512-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2512-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2512-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2512-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2512-129">CommonParameters</span></span>
<span data-ttu-id="a2512-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2512-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2512-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2512-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2512-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2512-132">INPUTS</span></span>

### <span data-ttu-id="a2512-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a2512-133">System.String</span></span>

## <span data-ttu-id="a2512-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2512-134">OUTPUTS</span></span>

### <span data-ttu-id="a2512-135">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="a2512-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="a2512-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2512-136">NOTES</span></span>

## <span data-ttu-id="a2512-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2512-137">RELATED LINKS</span></span>

[<span data-ttu-id="a2512-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a2512-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="a2512-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a2512-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="a2512-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a2512-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a2512-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a2512-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a2512-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a2512-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)