---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066030"
---
# <span data-ttu-id="f23eb-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="f23eb-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="f23eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f23eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f23eb-103">Возвращает политику масок данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="f23eb-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="f23eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f23eb-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f23eb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f23eb-105">DESCRIPTION</span></span>
<span data-ttu-id="f23eb-106">Командлет **Get-AzSqlDatabaseDataMaskingPolicy** получает политику масок данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f23eb-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="f23eb-107">Для использования этого командлета используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="f23eb-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f23eb-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="f23eb-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f23eb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f23eb-109">EXAMPLES</span></span>

### <span data-ttu-id="f23eb-110">Пример 1: получение политики маскирования данных для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="f23eb-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="f23eb-111">Эта команда получает политику маскировки данных из Database01 базы данных в группе ресурсов ResourceGroup01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="f23eb-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="f23eb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f23eb-112">PARAMETERS</span></span>

### <span data-ttu-id="f23eb-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f23eb-113">-DatabaseName</span></span>
<span data-ttu-id="f23eb-114">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f23eb-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f23eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23eb-115">-DefaultProfile</span></span>
<span data-ttu-id="f23eb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f23eb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f23eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f23eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="f23eb-118">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="f23eb-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f23eb-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f23eb-119">-ServerName</span></span>
<span data-ttu-id="f23eb-120">Указывает имя сервера, на котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="f23eb-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="f23eb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f23eb-121">-Confirm</span></span>
<span data-ttu-id="f23eb-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f23eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f23eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f23eb-123">-WhatIf</span></span>
<span data-ttu-id="f23eb-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f23eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f23eb-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f23eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f23eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23eb-126">CommonParameters</span></span>
<span data-ttu-id="f23eb-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f23eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23eb-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f23eb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23eb-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f23eb-129">INPUTS</span></span>

### <span data-ttu-id="f23eb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f23eb-130">System.String</span></span>

## <span data-ttu-id="f23eb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f23eb-131">OUTPUTS</span></span>

### <span data-ttu-id="f23eb-132">Microsoft. Azure. Commands. SQL. маскирует. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f23eb-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="f23eb-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f23eb-133">NOTES</span></span>

## <span data-ttu-id="f23eb-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f23eb-134">RELATED LINKS</span></span>

[<span data-ttu-id="f23eb-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f23eb-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f23eb-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f23eb-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f23eb-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f23eb-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f23eb-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="f23eb-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="f23eb-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f23eb-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


