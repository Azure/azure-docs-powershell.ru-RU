---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: d160e6cf954240495a9f9b3969d87dab6d880e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906217"
---
# <span data-ttu-id="fd2e9-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd2e9-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="fd2e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2e9-103">Возвращает политику безопасного подключения для базы данных.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-103">Gets the secure connection policy for a database.</span></span> <span data-ttu-id="fd2e9-104">Безопасное соединение устарело, и эта команда будет удалена в будущем выпуске.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-104">Secure connection is deprecated and this command will be removed in a future release.</span></span> <span data-ttu-id="fd2e9-105">Чтобы просмотреть строки подключения, используйте блейд-базу данных SQL на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-105">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

## <span data-ttu-id="fd2e9-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd2e9-106">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd2e9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd2e9-107">DESCRIPTION</span></span>
<span data-ttu-id="fd2e9-108">Командлет **Get-AzSqlDatabaseSecureConnectionPolicy** получает политику зашифрованных каналов для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-108">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="fd2e9-109">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="fd2e9-110">После успешного запуска этого командлета возвращается объект, который описывает текущую политику шифрования канала и идентификаторы базы данных.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-110">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="fd2e9-111">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="fd2e9-112">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fd2e9-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd2e9-113">EXAMPLES</span></span>

### <span data-ttu-id="fd2e9-114">Пример 1: получение политики зашифрованных каналов для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="fd2e9-114">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="fd2e9-115">Эта команда получает политику зашифрованных каналов для базы данных Azure SQL с именем Database01, расположенную на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-115">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="fd2e9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd2e9-116">PARAMETERS</span></span>

### <span data-ttu-id="fd2e9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd2e9-117">-DatabaseName</span></span>
<span data-ttu-id="fd2e9-118">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-118">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fd2e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2e9-119">-DefaultProfile</span></span>
<span data-ttu-id="fd2e9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fd2e9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd2e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd2e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="fd2e9-122">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fd2e9-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fd2e9-123">-ServerName</span></span>
<span data-ttu-id="fd2e9-124">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-124">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="fd2e9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd2e9-125">-Confirm</span></span>
<span data-ttu-id="fd2e9-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd2e9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd2e9-127">-WhatIf</span></span>
<span data-ttu-id="fd2e9-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd2e9-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd2e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2e9-130">CommonParameters</span></span>
<span data-ttu-id="fd2e9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd2e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2e9-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd2e9-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2e9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd2e9-133">INPUTS</span></span>

### <span data-ttu-id="fd2e9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fd2e9-134">System.String</span></span>

## <span data-ttu-id="fd2e9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd2e9-135">OUTPUTS</span></span>

### <span data-ttu-id="fd2e9-136">Microsoft. Azure. Commands. SQL. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fd2e9-136">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="fd2e9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd2e9-137">NOTES</span></span>

## <span data-ttu-id="fd2e9-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd2e9-138">RELATED LINKS</span></span>
