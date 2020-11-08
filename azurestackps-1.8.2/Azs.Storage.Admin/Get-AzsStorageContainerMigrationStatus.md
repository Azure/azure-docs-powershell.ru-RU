---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076891"
---
# <span data-ttu-id="b0e85-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="b0e85-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="b0e85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0e85-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e85-103">Возвращает состояние задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="b0e85-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="b0e85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0e85-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0e85-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0e85-105">DESCRIPTION</span></span>
<span data-ttu-id="b0e85-106">Возвращает состояние задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="b0e85-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="b0e85-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0e85-107">EXAMPLES</span></span>

### <span data-ttu-id="b0e85-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="b0e85-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="b0e85-109">Получение состояния задания миграции контейнера.</span><span class="sxs-lookup"><span data-stu-id="b0e85-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="b0e85-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0e85-110">PARAMETERS</span></span>

### <span data-ttu-id="b0e85-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="b0e85-111">-FarmName</span></span>
<span data-ttu-id="b0e85-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="b0e85-112">Farm Id.</span></span>

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

### <span data-ttu-id="b0e85-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="b0e85-113">-JobId</span></span>
<span data-ttu-id="b0e85-114">Код операции.</span><span class="sxs-lookup"><span data-stu-id="b0e85-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e85-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e85-115">-ResourceGroupName</span></span>
<span data-ttu-id="b0e85-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0e85-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e85-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e85-117">CommonParameters</span></span>
<span data-ttu-id="b0e85-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0e85-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e85-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e85-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e85-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0e85-120">INPUTS</span></span>

## <span data-ttu-id="b0e85-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0e85-121">OUTPUTS</span></span>

### <span data-ttu-id="b0e85-122">Microsoft. AzureStack. Management. Storage. admin. Models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="b0e85-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="b0e85-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0e85-123">NOTES</span></span>

## <span data-ttu-id="b0e85-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0e85-124">RELATED LINKS</span></span>
