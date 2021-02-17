---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243253"
---
# <span data-ttu-id="6982d-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6982d-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="6982d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6982d-102">SYNOPSIS</span></span>
<span data-ttu-id="6982d-103">Подготовка администратора Azure AD для SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6982d-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="6982d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6982d-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6982d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6982d-105">DESCRIPTION</span></span>
<span data-ttu-id="6982d-106">Для AzureSQL Server в текущей подписке предусмотрена учетная запись администратора **Set-AzSqlServerActiveDirectoryAdministrator.**</span><span class="sxs-lookup"><span data-stu-id="6982d-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="6982d-107">Одновременно можно втьть только одного администратора.</span><span class="sxs-lookup"><span data-stu-id="6982d-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="6982d-108">Следующими участниками Azure AD могут быть предусмотрены права SQL Server администратора:</span><span class="sxs-lookup"><span data-stu-id="6982d-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="6982d-109">Участники, которые являются участниками Azure AD</span><span class="sxs-lookup"><span data-stu-id="6982d-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="6982d-110">Федераированные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="6982d-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="6982d-111">Импортированные участники из других служб Azure ADs, которые являются родными или федеративными участниками</span><span class="sxs-lookup"><span data-stu-id="6982d-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="6982d-112">Группы Azure AD, созданные как учетные записи Майкрософт в качестве групп безопасности, например в доменах Outlook.com, Hotmail.com или Live.com, не поддерживаются администраторами.</span><span class="sxs-lookup"><span data-stu-id="6982d-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="6982d-113">Другие гостевых учетные записи, например учетные записи Gmail.com или Yahoo.com, не поддерживаются администраторами.</span><span class="sxs-lookup"><span data-stu-id="6982d-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="6982d-114">Мы рекомендуем на правах администратора использовать специальную группу Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6982d-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="6982d-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6982d-115">EXAMPLES</span></span>

### <span data-ttu-id="6982d-116">Пример 1. Подготовка группы администраторов для сервера</span><span class="sxs-lookup"><span data-stu-id="6982d-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="6982d-117">Эта команда предусматривает группу администраторов Azure AD с именем DBAs для сервера Server01.</span><span class="sxs-lookup"><span data-stu-id="6982d-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="6982d-118">Этот сервер связан с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6982d-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="6982d-119">Пример 2. Подготовка пользователя администратора к серверу</span><span class="sxs-lookup"><span data-stu-id="6982d-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="6982d-120">Эта команда служит для администратора сервера Server01 пользователя Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6982d-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="6982d-121">Пример 3. Подготовка группы администраторов с указанием ее ИД</span><span class="sxs-lookup"><span data-stu-id="6982d-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="6982d-122">Эта команда предусматривает группу администраторов Azure AD с именем DBAs для сервера Server01.</span><span class="sxs-lookup"><span data-stu-id="6982d-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="6982d-123">Команда определяет ИД параметра *ObjectId.*</span><span class="sxs-lookup"><span data-stu-id="6982d-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="6982d-124">Это позволяет добиться успеха команды, даже если отображаемое имя группы не уникально.</span><span class="sxs-lookup"><span data-stu-id="6982d-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="6982d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6982d-125">PARAMETERS</span></span>

### <span data-ttu-id="6982d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6982d-126">-DefaultProfile</span></span>
<span data-ttu-id="6982d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6982d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6982d-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6982d-128">-DisplayName</span></span>
<span data-ttu-id="6982d-129">Указывает отображаемого имя администратора Azure AD, которое предусмотрено этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6982d-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="6982d-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6982d-130">-ObjectId</span></span>
<span data-ttu-id="6982d-131">Указывает уникальный код администратора Azure AD, который требуется для этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6982d-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="6982d-132">Если отображаемое имя не уникально, необходимо указать значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="6982d-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6982d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6982d-133">-ResourceGroupName</span></span>
<span data-ttu-id="6982d-134">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="6982d-134">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6982d-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6982d-135">-ServerName</span></span>
<span data-ttu-id="6982d-136">Указывает имя учетной записи SQL Server для которой данный cmdlet предусматривает права администратора.</span><span class="sxs-lookup"><span data-stu-id="6982d-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6982d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6982d-137">-Confirm</span></span>
<span data-ttu-id="6982d-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6982d-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6982d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6982d-139">-WhatIf</span></span>
<span data-ttu-id="6982d-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6982d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6982d-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6982d-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6982d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6982d-142">CommonParameters</span></span>
<span data-ttu-id="6982d-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6982d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6982d-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6982d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6982d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6982d-145">INPUTS</span></span>

### <span data-ttu-id="6982d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="6982d-146">System.String</span></span>

### <span data-ttu-id="6982d-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6982d-147">System.Guid</span></span>

## <span data-ttu-id="6982d-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6982d-148">OUTPUTS</span></span>

### <span data-ttu-id="6982d-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="6982d-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="6982d-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6982d-150">NOTES</span></span>

## <span data-ttu-id="6982d-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6982d-151">RELATED LINKS</span></span>

[<span data-ttu-id="6982d-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6982d-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="6982d-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6982d-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="6982d-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="6982d-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="6982d-155">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="6982d-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


