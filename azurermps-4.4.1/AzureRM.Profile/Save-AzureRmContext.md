---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 5c6200f6d68760cbd93460b38cb72a379845e622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733346"
---
# <span data-ttu-id="730c2-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="730c2-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="730c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="730c2-102">SYNOPSIS</span></span>
<span data-ttu-id="730c2-103">Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="730c2-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="730c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="730c2-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="730c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="730c2-105">DESCRIPTION</span></span>
<span data-ttu-id="730c2-106">Командлет Save-AzureRmContext сохраняет текущие сведения для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="730c2-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="730c2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="730c2-107">EXAMPLES</span></span>

### <span data-ttu-id="730c2-108">Пример 1: Сохранение контекста текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="730c2-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="730c2-109">В этом примере контекст Azure текущего сеанса сохраняется в указанном JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="730c2-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="730c2-110">Пример 2: сохранение определенного контекста</span><span class="sxs-lookup"><span data-stu-id="730c2-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="730c2-111">В этом примере выполняется сохранение контекста Azure, который передается в командлет, в указанный JSON файл.</span><span class="sxs-lookup"><span data-stu-id="730c2-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="730c2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="730c2-112">PARAMETERS</span></span>

### <span data-ttu-id="730c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="730c2-113">-DefaultProfile</span></span>
<span data-ttu-id="730c2-114">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="730c2-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="730c2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="730c2-115">-Force</span></span>
<span data-ttu-id="730c2-116">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="730c2-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="730c2-117">-Path</span><span class="sxs-lookup"><span data-stu-id="730c2-117">-Path</span></span>
<span data-ttu-id="730c2-118">Задает путь к файлу, в который нужно сохранить сведения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="730c2-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="730c2-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="730c2-119">-Profile</span></span>
<span data-ttu-id="730c2-120">Указывает контекст Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="730c2-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="730c2-121">Если контекст не указан, этот командлет считывает данные из локального контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="730c2-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="730c2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="730c2-122">-Confirm</span></span>
<span data-ttu-id="730c2-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="730c2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="730c2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="730c2-124">-WhatIf</span></span>
<span data-ttu-id="730c2-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="730c2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="730c2-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="730c2-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="730c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="730c2-127">CommonParameters</span></span>
<span data-ttu-id="730c2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="730c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="730c2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="730c2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="730c2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="730c2-130">INPUTS</span></span>

### <span data-ttu-id="730c2-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="730c2-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="730c2-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="730c2-132">OUTPUTS</span></span>

### <span data-ttu-id="730c2-133">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="730c2-133">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="730c2-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="730c2-134">NOTES</span></span>

## <span data-ttu-id="730c2-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="730c2-135">RELATED LINKS</span></span>

