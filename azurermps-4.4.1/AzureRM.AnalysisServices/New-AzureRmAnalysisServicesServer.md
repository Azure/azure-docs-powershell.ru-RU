---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558052"
---
# <span data-ttu-id="6d50f-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6d50f-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="6d50f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d50f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d50f-103">Создание сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6d50f-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d50f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d50f-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d50f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d50f-105">DESCRIPTION</span></span>
<span data-ttu-id="6d50f-106">Командлет New-AzureRmAnalysisServicesServer создает новый сервер служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="6d50f-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="6d50f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d50f-107">EXAMPLES</span></span>

### <span data-ttu-id="6d50f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d50f-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="6d50f-109">Создание сервера с именем TestServer в Azure Region Запад — US и в группе ресурсов testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="6d50f-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="6d50f-110">Уровень SKU для сервера будет равен S1.</span><span class="sxs-lookup"><span data-stu-id="6d50f-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="6d50f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d50f-111">PARAMETERS</span></span>

### <span data-ttu-id="6d50f-112">-Администратор</span><span class="sxs-lookup"><span data-stu-id="6d50f-112">-Administrator</span></span>
<span data-ttu-id="6d50f-113">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="6d50f-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="6d50f-114">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="6d50f-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d50f-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="6d50f-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="6d50f-116">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6d50f-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d50f-117">-Location</span><span class="sxs-lookup"><span data-stu-id="6d50f-117">-Location</span></span>
<span data-ttu-id="6d50f-118">Регион Azure, на котором размещен сервер служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6d50f-118">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d50f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d50f-119">-Name</span></span>
<span data-ttu-id="6d50f-120">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6d50f-120">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="6d50f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d50f-121">-ResourceGroupName</span></span>
<span data-ttu-id="6d50f-122">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="6d50f-122">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="6d50f-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="6d50f-123">-Sku</span></span>
<span data-ttu-id="6d50f-124">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="6d50f-124">The name of the Sku for the server.</span></span>
<span data-ttu-id="6d50f-125">Поддерживаются значения 0 ", 1", "2" и "4" для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="6d50f-125">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d50f-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="6d50f-126">-Tag</span></span>
<span data-ttu-id="6d50f-127">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="6d50f-127">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d50f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d50f-128">-Confirm</span></span>
<span data-ttu-id="6d50f-129">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="6d50f-129">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d50f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d50f-130">-WhatIf</span></span>
<span data-ttu-id="6d50f-131">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="6d50f-131">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d50f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d50f-132">CommonParameters</span></span>
<span data-ttu-id="6d50f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d50f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d50f-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d50f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d50f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d50f-135">INPUTS</span></span>

## <span data-ttu-id="6d50f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d50f-136">OUTPUTS</span></span>

### <span data-ttu-id="6d50f-137">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6d50f-137">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="6d50f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d50f-138">NOTES</span></span>
<span data-ttu-id="6d50f-139">Alias (псевдоним): New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="6d50f-139">Alias: New-AzureAs</span></span>

## <span data-ttu-id="6d50f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d50f-140">RELATED LINKS</span></span>

[<span data-ttu-id="6d50f-141">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6d50f-141">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="6d50f-142">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6d50f-142">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
