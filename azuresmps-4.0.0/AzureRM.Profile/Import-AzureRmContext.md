---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554915"
---
# <span data-ttu-id="f3587-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f3587-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="f3587-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3587-102">SYNOPSIS</span></span>
<span data-ttu-id="f3587-103">Загрузка данных проверки подлинности Azure из файла.</span><span class="sxs-lookup"><span data-stu-id="f3587-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="f3587-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3587-104">SYNTAX</span></span>

### <span data-ttu-id="f3587-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="f3587-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3587-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="f3587-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f3587-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3587-107">DESCRIPTION</span></span>
<span data-ttu-id="f3587-108">Командлет Import-AzureRmContext загружает данные для проверки подлинности из файла, чтобы установить среду и контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="f3587-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="f3587-109">Командлеты, выполняемые в текущем сеансе, используют эти сведения для проверки подлинности запросов в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f3587-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="f3587-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3587-110">EXAMPLES</span></span>

### <span data-ttu-id="f3587-111">Пример 1: импорт контекста из AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="f3587-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="f3587-112">В этом примере выполняется импорт контекста из PSAzureProfile, который передается в командлет.</span><span class="sxs-lookup"><span data-stu-id="f3587-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="f3587-113">Пример 2: импорт контекста из JSON-файла</span><span class="sxs-lookup"><span data-stu-id="f3587-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="f3587-114">В этом примере выделяется контекст из JSON-файла, который передается в командлет.</span><span class="sxs-lookup"><span data-stu-id="f3587-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="f3587-115">Этот JSON-файл можно создать из импорта — AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="f3587-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="f3587-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3587-116">PARAMETERS</span></span>

### <span data-ttu-id="f3587-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="f3587-117">-AzureContext</span></span>
<span data-ttu-id="f3587-118">Указывает контекст Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3587-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="f3587-119">Если контекст не указан, этот командлет считывает данные из локального контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3587-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3587-120">-Path</span><span class="sxs-lookup"><span data-stu-id="f3587-120">-Path</span></span>
<span data-ttu-id="f3587-121">Указывает путь к контекстной информации, сохраненной с помощью команды Save-AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="f3587-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3587-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3587-122">-Confirm</span></span>
<span data-ttu-id="f3587-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3587-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3587-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3587-124">-WhatIf</span></span>
<span data-ttu-id="f3587-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3587-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3587-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3587-126">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f3587-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3587-127">INPUTS</span></span>

### <span data-ttu-id="f3587-128">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="f3587-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="f3587-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f3587-129">System.String</span></span>

## <span data-ttu-id="f3587-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3587-130">OUTPUTS</span></span>

### <span data-ttu-id="f3587-131">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f3587-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="f3587-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3587-132">NOTES</span></span>

## <span data-ttu-id="f3587-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3587-133">RELATED LINKS</span></span>

