---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 42e268a36cf6ea45d4a36ef1a7c3edd825c6e8ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566138"
---
# <span data-ttu-id="5c666-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c666-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="5c666-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c666-102">SYNOPSIS</span></span>
<span data-ttu-id="5c666-103">Поиск групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c666-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c666-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c666-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c666-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c666-105">DESCRIPTION</span></span>
<span data-ttu-id="5c666-106">Командлет **Find-AzureRmResourceGroup** выполняет поиск групп ресурсов с использованием указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="5c666-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="5c666-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c666-107">EXAMPLES</span></span>

### <span data-ttu-id="5c666-108">Пример 1: Поиск всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="5c666-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="5c666-109">Эта команда находит все группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c666-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="5c666-110">Пример 2: Поиск групп ресурсов по названию тега</span><span class="sxs-lookup"><span data-stu-id="5c666-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="5c666-111">Эта команда находит все группы ресурсов, у которых есть тег с именем testtag.</span><span class="sxs-lookup"><span data-stu-id="5c666-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="5c666-112">Пример 3: Поиск групп ресурсов по имени и значению тега</span><span class="sxs-lookup"><span data-stu-id="5c666-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="5c666-113">Эта команда находит все группы ресурсов, у которых есть тег с именем testtag, и значение testval.</span><span class="sxs-lookup"><span data-stu-id="5c666-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="5c666-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c666-114">PARAMETERS</span></span>

### <span data-ttu-id="5c666-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5c666-115">-ApiVersion</span></span>
<span data-ttu-id="5c666-116">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c666-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="5c666-117">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="5c666-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5c666-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c666-118">-DefaultProfile</span></span>
<span data-ttu-id="5c666-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5c666-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c666-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="5c666-120">-Pre</span></span>
<span data-ttu-id="5c666-121">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="5c666-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c666-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="5c666-122">-Tag</span></span>
<span data-ttu-id="5c666-123">Определяет сведения о теге в виде хэш-таблицы, чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="5c666-123">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="5c666-124">Используйте следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="5c666-124">Use the following formats:</span></span>

<span data-ttu-id="5c666-125">@ {tagName = $null} или @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="5c666-125">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c666-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c666-126">CommonParameters</span></span>
<span data-ttu-id="5c666-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c666-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c666-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c666-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c666-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c666-129">INPUTS</span></span>

### <span data-ttu-id="5c666-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="5c666-130">None</span></span>
<span data-ttu-id="5c666-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5c666-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c666-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c666-132">OUTPUTS</span></span>

### <span data-ttu-id="5c666-133">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5c666-133">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5c666-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c666-134">NOTES</span></span>

## <span data-ttu-id="5c666-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c666-135">RELATED LINKS</span></span>
