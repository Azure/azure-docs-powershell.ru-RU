---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243865"
---
# <span data-ttu-id="ce64d-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ce64d-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="ce64d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce64d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce64d-103">Подготовка администратора Azure AD к SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ce64d-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="ce64d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce64d-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce64d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce64d-105">DESCRIPTION</span></span>
<span data-ttu-id="ce64d-106">Командлет **Set-AzSqlServerActiveDirectoryAdministrator** подготавливает администратора Azure Active Directory (Azure AD) для AzureSQL Server в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="ce64d-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="ce64d-107">Вы можете подготовить только одного администратора за один раз.</span><span class="sxs-lookup"><span data-stu-id="ce64d-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="ce64d-108">Следующие участники Azure AD могут быть предоставлены в качестве администратора SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ce64d-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="ce64d-109">Собственные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="ce64d-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="ce64d-110">Федеративные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="ce64d-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="ce64d-111">Импортированные члены из других рекламных объявлений Azure, которые являются собственными или федеративными участниками</span><span class="sxs-lookup"><span data-stu-id="ce64d-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="ce64d-112">Группы Azure AD, созданные как группы безопасности учетные записи Майкрософт (например, в доменах Outlook.com, Hotmail.com или Live.com), не поддерживаются как администраторы.</span><span class="sxs-lookup"><span data-stu-id="ce64d-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="ce64d-113">Другие гостевые учетные записи, например в доменах Gmail.com и Yahoo.com, не поддерживаются в качестве администраторов.</span><span class="sxs-lookup"><span data-stu-id="ce64d-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="ce64d-114">Рекомендуем предоставить специальную группу Azure AD в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="ce64d-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="ce64d-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce64d-115">EXAMPLES</span></span>

### <span data-ttu-id="ce64d-116">Пример 1: подготовка группы администраторов для сервера</span><span class="sxs-lookup"><span data-stu-id="ce64d-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="ce64d-117">Эта команда подготавливает группу администраторов Azure Active Directory с именем "Администраторы доменных имен" для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="ce64d-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="ce64d-118">Этот сервер связан с группой ResourceGroup01 ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce64d-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="ce64d-119">Пример 2: предоставление пользователю администратора сервера</span><span class="sxs-lookup"><span data-stu-id="ce64d-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="ce64d-120">Эта команда подготавливает пользователя Azure AD к учетной записи администратора сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="ce64d-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="ce64d-121">Пример 3: предоставление группы администраторов с указанием ее идентификатора</span><span class="sxs-lookup"><span data-stu-id="ce64d-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="ce64d-122">Эта команда подготавливает группу администраторов Azure Active Directory с именем "Администраторы доменных имен" для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="ce64d-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="ce64d-123">Команда задает идентификатор для параметра *ObjectID* .</span><span class="sxs-lookup"><span data-stu-id="ce64d-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="ce64d-124">Это гарантирует, что команда будет выполнена успешно, даже если отображаемое имя группы не является уникальным.</span><span class="sxs-lookup"><span data-stu-id="ce64d-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="ce64d-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce64d-125">PARAMETERS</span></span>

### <span data-ttu-id="ce64d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce64d-126">-DefaultProfile</span></span>
<span data-ttu-id="ce64d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ce64d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce64d-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ce64d-128">-DisplayName</span></span>
<span data-ttu-id="ce64d-129">Указывает отображаемое имя администратора Active Directory для Azure, которое подготавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ce64d-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="ce64d-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ce64d-130">-ObjectId</span></span>
<span data-ttu-id="ce64d-131">Указывает уникальный идентификатор администратора Azure AD, который подготавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ce64d-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="ce64d-132">Если отображаемое имя не является уникальным, необходимо указать значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="ce64d-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="ce64d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce64d-133">-ResourceGroupName</span></span>
<span data-ttu-id="ce64d-134">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="ce64d-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ce64d-135">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ce64d-135">-ServerName</span></span>
<span data-ttu-id="ce64d-136">Указывает имя сервера SQL Server, для которого этот командлет подготавливает администратора.</span><span class="sxs-lookup"><span data-stu-id="ce64d-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="ce64d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce64d-137">-Confirm</span></span>
<span data-ttu-id="ce64d-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce64d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce64d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce64d-139">-WhatIf</span></span>
<span data-ttu-id="ce64d-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce64d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce64d-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce64d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce64d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce64d-142">CommonParameters</span></span>
<span data-ttu-id="ce64d-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce64d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce64d-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce64d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce64d-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce64d-145">INPUTS</span></span>

### <span data-ttu-id="ce64d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ce64d-146">System.String</span></span>

### <span data-ttu-id="ce64d-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ce64d-147">System.Guid</span></span>

## <span data-ttu-id="ce64d-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce64d-148">OUTPUTS</span></span>

### <span data-ttu-id="ce64d-149">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="ce64d-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="ce64d-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce64d-150">NOTES</span></span>

## <span data-ttu-id="ce64d-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce64d-151">RELATED LINKS</span></span>

[<span data-ttu-id="ce64d-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ce64d-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ce64d-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ce64d-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="ce64d-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="ce64d-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="ce64d-155">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="ce64d-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


