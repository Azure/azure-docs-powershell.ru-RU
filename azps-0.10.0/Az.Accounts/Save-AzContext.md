---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 07e565031a5c29ae1be78246cad95326952007e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909377"
---
# <span data-ttu-id="57473-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="57473-101">Save-AzContext</span></span>

## <span data-ttu-id="57473-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57473-102">SYNOPSIS</span></span>
<span data-ttu-id="57473-103">Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="57473-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="57473-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57473-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57473-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57473-105">DESCRIPTION</span></span>
<span data-ttu-id="57473-106">Командлет Save-AzContext сохраняет текущие сведения для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="57473-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="57473-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57473-107">EXAMPLES</span></span>

### <span data-ttu-id="57473-108">Пример 1: Сохранение контекста текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="57473-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="57473-109">В этом примере контекст Azure текущего сеанса сохраняется в указанном JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="57473-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="57473-110">Пример 2: сохранение определенного контекста</span><span class="sxs-lookup"><span data-stu-id="57473-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="57473-111">В этом примере выполняется сохранение контекста Azure, который передается в командлет, в указанный JSON файл.</span><span class="sxs-lookup"><span data-stu-id="57473-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="57473-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57473-112">PARAMETERS</span></span>

### <span data-ttu-id="57473-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57473-113">-DefaultProfile</span></span>
<span data-ttu-id="57473-114">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57473-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57473-115">-Force</span><span class="sxs-lookup"><span data-stu-id="57473-115">-Force</span></span>
<span data-ttu-id="57473-116">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="57473-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="57473-117">-Path</span><span class="sxs-lookup"><span data-stu-id="57473-117">-Path</span></span>
<span data-ttu-id="57473-118">Задает путь к файлу, в который нужно сохранить сведения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="57473-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="57473-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="57473-119">-Profile</span></span>
<span data-ttu-id="57473-120">Указывает контекст Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="57473-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="57473-121">Если контекст не указан, этот командлет считывает данные из локального контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57473-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="57473-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57473-122">-Confirm</span></span>
<span data-ttu-id="57473-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57473-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57473-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57473-124">-WhatIf</span></span>
<span data-ttu-id="57473-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57473-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57473-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57473-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57473-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57473-127">CommonParameters</span></span>
<span data-ttu-id="57473-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57473-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57473-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57473-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57473-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57473-130">INPUTS</span></span>

### <span data-ttu-id="57473-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="57473-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="57473-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57473-132">OUTPUTS</span></span>

### <span data-ttu-id="57473-133">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="57473-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="57473-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="57473-134">NOTES</span></span>

## <span data-ttu-id="57473-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57473-135">RELATED LINKS</span></span>
