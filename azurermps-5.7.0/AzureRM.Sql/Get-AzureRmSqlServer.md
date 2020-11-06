---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: a3af56ab78cd31dde30939901eaff12fff78ffa2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567389"
---
# <span data-ttu-id="6b871-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6b871-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="6b871-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b871-102">SYNOPSIS</span></span>
<span data-ttu-id="6b871-103">Возвращает сведения о серверах баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="6b871-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b871-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b871-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b871-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b871-105">DESCRIPTION</span></span>
<span data-ttu-id="6b871-106">Командлет **Get-AzureRmSqlServer** возвращает сведения об одном или нескольких серверах баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6b871-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="6b871-107">Укажите имя сервера, чтобы просмотреть сведения только для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="6b871-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="6b871-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b871-108">EXAMPLES</span></span>

### <span data-ttu-id="6b871-109">Пример 1: получение всех экземпляров сервера SQL Server, назначенных группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="6b871-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="6b871-110">Эта команда получает сведения обо всех серверах баз данных SQL Azure, назначенных группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6b871-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="6b871-111">Пример 2: получение сведений о сервере базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="6b871-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="6b871-112">Эта команда получает сведения о сервере базы данных SQL Azure с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="6b871-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="6b871-113">Пример 3: получение всех экземпляров SQL Server в подписке</span><span class="sxs-lookup"><span data-stu-id="6b871-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="6b871-114">Эта команда получает сведения обо всех серверах баз данных SQL Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="6b871-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="6b871-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b871-115">PARAMETERS</span></span>

### <span data-ttu-id="6b871-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b871-116">-DefaultProfile</span></span>
<span data-ttu-id="6b871-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b871-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b871-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b871-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b871-119">Указывает имя группы ресурсов, которой назначены серверы.</span><span class="sxs-lookup"><span data-stu-id="6b871-119">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b871-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6b871-120">-ServerName</span></span>
<span data-ttu-id="6b871-121">Указывает имя сервера, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6b871-121">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b871-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b871-122">-Confirm</span></span>
<span data-ttu-id="6b871-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b871-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b871-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b871-124">-WhatIf</span></span>
<span data-ttu-id="6b871-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b871-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b871-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b871-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b871-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b871-127">CommonParameters</span></span>
<span data-ttu-id="6b871-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b871-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b871-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b871-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b871-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b871-130">INPUTS</span></span>

### <span data-ttu-id="6b871-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="6b871-131">None</span></span>
<span data-ttu-id="6b871-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6b871-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b871-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b871-133">OUTPUTS</span></span>

### <span data-ttu-id="6b871-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="6b871-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="6b871-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b871-135">NOTES</span></span>

## <span data-ttu-id="6b871-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b871-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b871-137">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6b871-137">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="6b871-138">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6b871-138">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="6b871-139">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6b871-139">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="6b871-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="6b871-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


