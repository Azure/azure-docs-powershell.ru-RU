---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ae4564b1f583b8057438ee631de6b13d38e008ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734210"
---
# <span data-ttu-id="45a1c-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="45a1c-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="45a1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="45a1c-103">Запускает рабочий процесс, который запускает рекомендованную операцию с индексами.</span><span class="sxs-lookup"><span data-stu-id="45a1c-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45a1c-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45a1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="45a1c-106">Командлет **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** запускает рабочий процесс, который запускает рекомендованную операцию с индексами для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="45a1c-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="45a1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="45a1c-108">Пример 1: выполнение рекомендации по индексу</span><span class="sxs-lookup"><span data-stu-id="45a1c-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="45a1c-109">Эта команда запускает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="45a1c-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="45a1c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="45a1c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45a1c-111">-DatabaseName</span></span>
<span data-ttu-id="45a1c-112">Указывает имя базы данных, для которой этот командлет запускает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="45a1c-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a1c-113">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="45a1c-113">-IndexRecommendationName</span></span>
<span data-ttu-id="45a1c-114">Указывает имя рекомендации по индексированию, которое будет запущено этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="45a1c-114">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a1c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a1c-115">-ResourceGroupName</span></span>
<span data-ttu-id="45a1c-116">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="45a1c-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="45a1c-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="45a1c-117">-ServerName</span></span>
<span data-ttu-id="45a1c-118">Указывает сервер, на котором размещена база данных, для которой этот командлет запускает рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="45a1c-118">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a1c-119">-DefaultProfile</span></span>
<span data-ttu-id="45a1c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45a1c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45a1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a1c-121">CommonParameters</span></span>
<span data-ttu-id="45a1c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45a1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a1c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a1c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a1c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45a1c-124">INPUTS</span></span>

## <span data-ttu-id="45a1c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45a1c-125">OUTPUTS</span></span>

## <span data-ttu-id="45a1c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="45a1c-126">NOTES</span></span>

## <span data-ttu-id="45a1c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45a1c-127">RELATED LINKS</span></span>

[<span data-ttu-id="45a1c-128">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="45a1c-128">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="45a1c-129">Остановить-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="45a1c-129">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="45a1c-130">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="45a1c-130">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


