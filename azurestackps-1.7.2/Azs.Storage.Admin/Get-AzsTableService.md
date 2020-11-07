---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01b3c055873276a265859683e07cd9150ffedafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907242"
---
# <span data-ttu-id="679f6-101">Get-AzsTableService</span><span class="sxs-lookup"><span data-stu-id="679f6-101">Get-AzsTableService</span></span>

## <span data-ttu-id="679f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="679f6-102">SYNOPSIS</span></span>
<span data-ttu-id="679f6-103">Возвращает службу таблицы.</span><span class="sxs-lookup"><span data-stu-id="679f6-103">Returns the table service.</span></span>

## <span data-ttu-id="679f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="679f6-104">SYNTAX</span></span>

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="679f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="679f6-105">DESCRIPTION</span></span>
<span data-ttu-id="679f6-106">Возвращает службу таблицы.</span><span class="sxs-lookup"><span data-stu-id="679f6-106">Returns the table service.</span></span>

## <span data-ttu-id="679f6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="679f6-107">EXAMPLES</span></span>

### <span data-ttu-id="679f6-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="679f6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="679f6-109">Получить таблицу servie.</span><span class="sxs-lookup"><span data-stu-id="679f6-109">Get the table servie.</span></span>

## <span data-ttu-id="679f6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="679f6-110">PARAMETERS</span></span>

### <span data-ttu-id="679f6-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="679f6-111">-FarmName</span></span>
<span data-ttu-id="679f6-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="679f6-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679f6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679f6-113">-ResourceGroupName</span></span>
<span data-ttu-id="679f6-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="679f6-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679f6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679f6-115">CommonParameters</span></span>
<span data-ttu-id="679f6-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="679f6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679f6-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="679f6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679f6-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="679f6-118">INPUTS</span></span>

## <span data-ttu-id="679f6-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="679f6-119">OUTPUTS</span></span>

### <span data-ttu-id="679f6-120">Microsoft. AzureStack. Management. Storage. admin. Models. TableService</span><span class="sxs-lookup"><span data-stu-id="679f6-120">Microsoft.AzureStack.Management.Storage.Admin.Models.TableService</span></span>

## <span data-ttu-id="679f6-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="679f6-121">NOTES</span></span>

## <span data-ttu-id="679f6-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="679f6-122">RELATED LINKS</span></span>

