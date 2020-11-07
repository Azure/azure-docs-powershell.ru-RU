---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 13ab762b7f5ed8457bc8975687c3a45315be969b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734762"
---
# <span data-ttu-id="fb827-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="fb827-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="fb827-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb827-102">SYNOPSIS</span></span>
<span data-ttu-id="fb827-103">Возвращает политику масок данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb827-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb827-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb827-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb827-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb827-105">DESCRIPTION</span></span>
<span data-ttu-id="fb827-106">Командлет **Get-AzureRmSqlDatabaseDataMaskingPolicy** получает политику масок данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fb827-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="fb827-107">Для использования этого командлета используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb827-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="fb827-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="fb827-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fb827-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb827-109">EXAMPLES</span></span>

### <span data-ttu-id="fb827-110">Пример 1: получение политики маскирования данных для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="fb827-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="fb827-111">Эта команда получает политику маскировки данных из Database01 базы данных в группе ресурсов ResourceGroup01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="fb827-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="fb827-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb827-112">PARAMETERS</span></span>

### <span data-ttu-id="fb827-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fb827-113">-DatabaseName</span></span>
<span data-ttu-id="fb827-114">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb827-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fb827-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb827-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb827-116">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="fb827-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="fb827-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fb827-117">-ServerName</span></span>
<span data-ttu-id="fb827-118">Указывает имя сервера, на котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="fb827-118">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="fb827-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb827-119">-Confirm</span></span>
<span data-ttu-id="fb827-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb827-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb827-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb827-121">-WhatIf</span></span>
<span data-ttu-id="fb827-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb827-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb827-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb827-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb827-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb827-124">-DefaultProfile</span></span>
<span data-ttu-id="fb827-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb827-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb827-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb827-126">CommonParameters</span></span>
<span data-ttu-id="fb827-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb827-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb827-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb827-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb827-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb827-129">INPUTS</span></span>

## <span data-ttu-id="fb827-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb827-130">OUTPUTS</span></span>

### <span data-ttu-id="fb827-131">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fb827-131">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="fb827-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb827-132">NOTES</span></span>

## <span data-ttu-id="fb827-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb827-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb827-134">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fb827-134">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fb827-135">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fb827-135">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fb827-136">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fb827-136">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="fb827-137">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="fb827-137">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="fb827-138">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="fb827-138">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


