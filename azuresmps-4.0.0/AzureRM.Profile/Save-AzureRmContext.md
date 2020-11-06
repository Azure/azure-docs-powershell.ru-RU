---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554916"
---
# <span data-ttu-id="7cd21-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="7cd21-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="7cd21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cd21-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd21-103">Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7cd21-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="7cd21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cd21-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7cd21-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cd21-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd21-106">Командлет Save-AzureRmContext сохраняет текущие сведения для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7cd21-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="7cd21-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cd21-107">EXAMPLES</span></span>

### <span data-ttu-id="7cd21-108">Пример 1: Сохранение контекста текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="7cd21-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="7cd21-109">В этом примере контекст Azure текущего сеанса сохраняется в указанном JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="7cd21-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="7cd21-110">Пример 2: сохранение определенного контекста</span><span class="sxs-lookup"><span data-stu-id="7cd21-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="7cd21-111">В этом примере выполняется сохранение контекста Azure, который передается в командлет, в указанный JSON файл.</span><span class="sxs-lookup"><span data-stu-id="7cd21-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="7cd21-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cd21-112">PARAMETERS</span></span>

### <span data-ttu-id="7cd21-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7cd21-113">-Force</span></span>
<span data-ttu-id="7cd21-114">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="7cd21-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd21-115">-Path</span><span class="sxs-lookup"><span data-stu-id="7cd21-115">-Path</span></span>
<span data-ttu-id="7cd21-116">Задает путь к файлу, в который нужно сохранить сведения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7cd21-116">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="7cd21-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="7cd21-117">-Profile</span></span>
<span data-ttu-id="7cd21-118">Указывает контекст Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7cd21-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="7cd21-119">Если контекст не указан, этот командлет считывает данные из локального контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7cd21-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd21-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cd21-120">-Confirm</span></span>
<span data-ttu-id="7cd21-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7cd21-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd21-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd21-122">-WhatIf</span></span>
<span data-ttu-id="7cd21-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7cd21-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd21-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7cd21-124">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="7cd21-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cd21-125">INPUTS</span></span>

### <span data-ttu-id="7cd21-126">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="7cd21-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="7cd21-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cd21-127">OUTPUTS</span></span>

### <span data-ttu-id="7cd21-128">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="7cd21-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="7cd21-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cd21-129">NOTES</span></span>

## <span data-ttu-id="7cd21-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cd21-130">RELATED LINKS</span></span>

