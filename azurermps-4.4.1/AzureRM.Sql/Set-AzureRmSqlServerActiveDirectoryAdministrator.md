---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566267"
---
# <span data-ttu-id="75756-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="75756-101">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="75756-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75756-102">SYNOPSIS</span></span>
<span data-ttu-id="75756-103">Подготовка администратора Azure AD к SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75756-103">Provisions an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75756-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75756-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75756-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75756-105">DESCRIPTION</span></span>
<span data-ttu-id="75756-106">Командлет **Set-AzureRmSqlServerActiveDirectoryAdministrator** подготавливает администратора Azure Active Directory (Azure AD) для AzureSQL Server в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="75756-106">The **Set-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

<span data-ttu-id="75756-107">Вы можете подготовить только одного администратора за один раз.</span><span class="sxs-lookup"><span data-stu-id="75756-107">You can provision only one administrator at a time.</span></span>

<span data-ttu-id="75756-108">Следующие участники Azure AD могут быть предоставлены в качестве администратора SQL Server:</span><span class="sxs-lookup"><span data-stu-id="75756-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>

- <span data-ttu-id="75756-109">Собственные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="75756-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="75756-110">Федеративные участники Azure AD</span><span class="sxs-lookup"><span data-stu-id="75756-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="75756-111">Импортированные члены из других рекламных объявлений Azure, которые являются собственными или федеративными участниками</span><span class="sxs-lookup"><span data-stu-id="75756-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="75756-112">Группы Azure AD, созданные как группы безопасности</span><span class="sxs-lookup"><span data-stu-id="75756-112">Azure AD groups created as security groups</span></span>

<span data-ttu-id="75756-113">Учетные записи Майкрософт, например, в доменах Outlook.com, Hotmail.com или Live.com, не поддерживаются в качестве администраторов.</span><span class="sxs-lookup"><span data-stu-id="75756-113">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="75756-114">Другие гостевые учетные записи, например в доменах Gmail.com и Yahoo.com, не поддерживаются в качестве администраторов.</span><span class="sxs-lookup"><span data-stu-id="75756-114">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>

<span data-ttu-id="75756-115">Рекомендуем предоставить специальную группу Azure AD в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="75756-115">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="75756-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75756-116">EXAMPLES</span></span>

### <span data-ttu-id="75756-117">Пример 1: подготовка группы администраторов для сервера</span><span class="sxs-lookup"><span data-stu-id="75756-117">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="75756-118">Эта команда подготавливает группу администраторов Azure Active Directory с именем "Администраторы доменных имен" для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="75756-118">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="75756-119">Этот сервер связан с группой ResourceGroup01 ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75756-119">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="75756-120">Пример 2: предоставление пользователю администратора сервера</span><span class="sxs-lookup"><span data-stu-id="75756-120">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="75756-121">Эта команда подготавливает пользователя Azure AD к учетной записи администратора сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="75756-121">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="75756-122">Пример 3: предоставление группы администраторов с указанием ее идентификатора</span><span class="sxs-lookup"><span data-stu-id="75756-122">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="75756-123">Эта команда подготавливает группу администраторов Azure Active Directory с именем "Администраторы доменных имен" для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="75756-123">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="75756-124">Команда задает идентификатор для параметра *ObjectID* .</span><span class="sxs-lookup"><span data-stu-id="75756-124">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="75756-125">Это гарантирует, что команда будет выполнена успешно, даже если отображаемое имя группы не является уникальным.</span><span class="sxs-lookup"><span data-stu-id="75756-125">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="75756-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75756-126">PARAMETERS</span></span>

### <span data-ttu-id="75756-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75756-127">-DisplayName</span></span>
<span data-ttu-id="75756-128">Указывает отображаемое имя администратора Active Directory для Azure, которое подготавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="75756-128">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="75756-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="75756-129">-ObjectId</span></span>
<span data-ttu-id="75756-130">Указывает уникальный идентификатор администратора Azure AD, который подготавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="75756-130">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="75756-131">Если отображаемое имя не является уникальным, необходимо указать значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="75756-131">If the display name is not unique, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="75756-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75756-132">-ResourceGroupName</span></span>
<span data-ttu-id="75756-133">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="75756-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="75756-134">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="75756-134">-ServerName</span></span>
<span data-ttu-id="75756-135">Указывает имя сервера SQL Server, для которого этот командлет подготавливает администратора.</span><span class="sxs-lookup"><span data-stu-id="75756-135">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="75756-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75756-136">-Confirm</span></span>
<span data-ttu-id="75756-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75756-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75756-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75756-138">-WhatIf</span></span>
<span data-ttu-id="75756-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75756-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75756-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75756-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75756-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75756-141">-DefaultProfile</span></span>
<span data-ttu-id="75756-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75756-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75756-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75756-143">CommonParameters</span></span>
<span data-ttu-id="75756-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75756-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75756-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75756-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75756-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75756-146">INPUTS</span></span>

## <span data-ttu-id="75756-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75756-147">OUTPUTS</span></span>

### <span data-ttu-id="75756-148">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="75756-148">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="75756-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="75756-149">NOTES</span></span>

## <span data-ttu-id="75756-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75756-150">RELATED LINKS</span></span>

[<span data-ttu-id="75756-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="75756-151">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="75756-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="75756-152">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="75756-153">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="75756-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


