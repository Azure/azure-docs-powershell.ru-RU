---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: 472e8e7a2f0919115686764136b6b40f5e1da913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563276"
---
# <span data-ttu-id="d2808-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="d2808-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="d2808-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2808-102">SYNOPSIS</span></span>
<span data-ttu-id="d2808-103">Возвращает базу данных и ее развернутые значения свойств.</span><span class="sxs-lookup"><span data-stu-id="d2808-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2808-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2808-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2808-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2808-105">DESCRIPTION</span></span>
<span data-ttu-id="d2808-106">Командлет **Get-AzureRmSqlDatabaseExpanded** получает базу данных и ее развернутые значения свойств.</span><span class="sxs-lookup"><span data-stu-id="d2808-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>

<span data-ttu-id="d2808-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="d2808-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d2808-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2808-108">EXAMPLES</span></span>

### <span data-ttu-id="d2808-109">Пример 1: получение объекта базы данных с данными советника по уровню обслуживания</span><span class="sxs-lookup"><span data-stu-id="d2808-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d2808-110">Эта команда возвращает базу данных с развернутыми свойствами, содержащими данные советника по уровню обслуживания.</span><span class="sxs-lookup"><span data-stu-id="d2808-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="d2808-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2808-111">PARAMETERS</span></span>

### <span data-ttu-id="d2808-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2808-112">-DatabaseName</span></span>
<span data-ttu-id="d2808-113">Указывает имя базы данных, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="d2808-113">Specifies the name of the database to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2808-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2808-114">-DefaultProfile</span></span>
<span data-ttu-id="d2808-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2808-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2808-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2808-116">-ResourceGroupName</span></span>
<span data-ttu-id="d2808-117">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="d2808-117">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2808-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d2808-118">-ServerName</span></span>
<span data-ttu-id="d2808-119">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="d2808-119">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2808-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2808-120">-Confirm</span></span>
<span data-ttu-id="d2808-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2808-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2808-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2808-122">-WhatIf</span></span>
<span data-ttu-id="d2808-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2808-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2808-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2808-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2808-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2808-125">CommonParameters</span></span>
<span data-ttu-id="d2808-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2808-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2808-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2808-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2808-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2808-128">INPUTS</span></span>

### <span data-ttu-id="d2808-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="d2808-129">None</span></span>
<span data-ttu-id="d2808-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d2808-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2808-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2808-131">OUTPUTS</span></span>

## <span data-ttu-id="d2808-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2808-132">NOTES</span></span>

## <span data-ttu-id="d2808-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2808-133">RELATED LINKS</span></span>

[<span data-ttu-id="d2808-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="d2808-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
