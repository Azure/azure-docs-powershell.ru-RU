---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076563"
---
# <span data-ttu-id="2bebc-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="2bebc-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="2bebc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2bebc-102">SYNOPSIS</span></span>
<span data-ttu-id="2bebc-103">Получает ограничение размера и размера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2bebc-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="2bebc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2bebc-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bebc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bebc-105">DESCRIPTION</span></span>
<span data-ttu-id="2bebc-106">Командлет **Get-AzureSqlDatabaseUsages** получает текущий размер и ограничение размера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2bebc-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="2bebc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2bebc-107">EXAMPLES</span></span>

### <span data-ttu-id="2bebc-108">Пример 1: получение сведений об использовании базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="2bebc-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="2bebc-109">Эта команда получает сведения о размере и размере для базы данных SQL с именем Database01 on Server01.</span><span class="sxs-lookup"><span data-stu-id="2bebc-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="2bebc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2bebc-110">PARAMETERS</span></span>

### <span data-ttu-id="2bebc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2bebc-111">-DatabaseName</span></span>
<span data-ttu-id="2bebc-112">Указывает имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2bebc-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bebc-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="2bebc-113">-Profile</span></span>
<span data-ttu-id="2bebc-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2bebc-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2bebc-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2bebc-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bebc-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2bebc-116">-ServerName</span></span>
<span data-ttu-id="2bebc-117">Указывает имя сервера, на котором размещена база данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2bebc-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bebc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bebc-118">CommonParameters</span></span>
<span data-ttu-id="2bebc-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2bebc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bebc-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bebc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bebc-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2bebc-121">INPUTS</span></span>

## <span data-ttu-id="2bebc-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bebc-122">OUTPUTS</span></span>

## <span data-ttu-id="2bebc-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="2bebc-123">NOTES</span></span>

## <span data-ttu-id="2bebc-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bebc-124">RELATED LINKS</span></span>

