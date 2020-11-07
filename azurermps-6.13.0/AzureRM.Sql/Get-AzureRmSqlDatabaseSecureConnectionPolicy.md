---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 92b75e55adb4e1107767c3c58394c9f344a5bd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733434"
---
# <span data-ttu-id="e7b98-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e7b98-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="e7b98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7b98-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b98-103">Возвращает политику безопасного подключения для базы данных.</span><span class="sxs-lookup"><span data-stu-id="e7b98-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7b98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7b98-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7b98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7b98-105">DESCRIPTION</span></span>
<span data-ttu-id="e7b98-106">Командлет **Get-AzureRmSqlDatabaseSecureConnectionPolicy** получает политику зашифрованных каналов для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e7b98-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="e7b98-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="e7b98-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e7b98-108">После успешного запуска этого командлета возвращается объект, который описывает текущую политику шифрования канала и идентификаторы базы данных.</span><span class="sxs-lookup"><span data-stu-id="e7b98-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="e7b98-109">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="e7b98-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="e7b98-110">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="e7b98-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e7b98-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7b98-111">EXAMPLES</span></span>

### <span data-ttu-id="e7b98-112">Пример 1: получение политики зашифрованных каналов для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e7b98-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="e7b98-113">Эта команда получает политику зашифрованных каналов для базы данных Azure SQL с именем Database01, расположенную на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="e7b98-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="e7b98-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7b98-114">PARAMETERS</span></span>

### <span data-ttu-id="e7b98-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7b98-115">-DatabaseName</span></span>
<span data-ttu-id="e7b98-116">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e7b98-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e7b98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b98-117">-DefaultProfile</span></span>
<span data-ttu-id="e7b98-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7b98-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7b98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b98-119">-ResourceGroupName</span></span>
<span data-ttu-id="e7b98-120">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="e7b98-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e7b98-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e7b98-121">-ServerName</span></span>
<span data-ttu-id="e7b98-122">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="e7b98-122">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="e7b98-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7b98-123">-Confirm</span></span>
<span data-ttu-id="e7b98-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7b98-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b98-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b98-125">-WhatIf</span></span>
<span data-ttu-id="e7b98-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7b98-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7b98-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7b98-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b98-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b98-128">CommonParameters</span></span>
<span data-ttu-id="e7b98-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7b98-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b98-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b98-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b98-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7b98-131">INPUTS</span></span>

### <span data-ttu-id="e7b98-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e7b98-132">System.String</span></span>

## <span data-ttu-id="e7b98-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7b98-133">OUTPUTS</span></span>

### <span data-ttu-id="e7b98-134">Microsoft. Azure. Commands. SQL. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e7b98-134">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="e7b98-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7b98-135">NOTES</span></span>

## <span data-ttu-id="e7b98-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7b98-136">RELATED LINKS</span></span>
