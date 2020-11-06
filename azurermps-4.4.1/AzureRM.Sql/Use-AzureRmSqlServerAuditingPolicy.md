---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566669"
---
# <span data-ttu-id="b23f9-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b23f9-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="b23f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b23f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b23f9-103">Указывает, что база данных использует политику аудита на своем хост-сервере.</span><span class="sxs-lookup"><span data-stu-id="b23f9-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b23f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b23f9-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b23f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b23f9-105">DESCRIPTION</span></span>
<span data-ttu-id="b23f9-106">Командлет **use-AzureRmSqlServerAuditingPolicy** указывает, что база данных использует политику аудита на своем хост-сервере.</span><span class="sxs-lookup"><span data-stu-id="b23f9-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="b23f9-107">Укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы идентифицировать базу данных.</span><span class="sxs-lookup"><span data-stu-id="b23f9-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b23f9-108">Если для сервера базы данных не определена политика аудита, этот командлет завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="b23f9-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="b23f9-109">Если узел использует аудит уровня сервера, обнаружение угроз удаляется.</span><span class="sxs-lookup"><span data-stu-id="b23f9-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="b23f9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b23f9-110">EXAMPLES</span></span>

### <span data-ttu-id="b23f9-111">Пример 1: Настройка базы данных для использования политики аудита сервера</span><span class="sxs-lookup"><span data-stu-id="b23f9-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="b23f9-112">Эта команда указывает на то, что база данных с именем Database01 on Server02 использует политику аудита сервера.</span><span class="sxs-lookup"><span data-stu-id="b23f9-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="b23f9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b23f9-113">PARAMETERS</span></span>

### <span data-ttu-id="b23f9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b23f9-114">-DatabaseName</span></span>
<span data-ttu-id="b23f9-115">Указывает имя базы данных, которая будет использовать политику аудита.</span><span class="sxs-lookup"><span data-stu-id="b23f9-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="b23f9-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b23f9-116">-PassThru</span></span>
<span data-ttu-id="b23f9-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b23f9-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b23f9-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b23f9-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b23f9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b23f9-119">-ResourceGroupName</span></span>
<span data-ttu-id="b23f9-120">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="b23f9-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b23f9-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b23f9-121">-ServerName</span></span>
<span data-ttu-id="b23f9-122">Указывает имя сервера, на котором размещается база данных, использующая политику аудита.</span><span class="sxs-lookup"><span data-stu-id="b23f9-122">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="b23f9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b23f9-123">-DefaultProfile</span></span>
<span data-ttu-id="b23f9-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b23f9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b23f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b23f9-125">CommonParameters</span></span>
<span data-ttu-id="b23f9-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b23f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b23f9-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b23f9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b23f9-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b23f9-128">INPUTS</span></span>

## <span data-ttu-id="b23f9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b23f9-129">OUTPUTS</span></span>

### <span data-ttu-id="b23f9-130">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b23f9-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="b23f9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b23f9-131">NOTES</span></span>

## <span data-ttu-id="b23f9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b23f9-132">RELATED LINKS</span></span>

[<span data-ttu-id="b23f9-133">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b23f9-133">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="b23f9-134">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b23f9-134">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="b23f9-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b23f9-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="b23f9-136">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b23f9-136">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="b23f9-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b23f9-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


