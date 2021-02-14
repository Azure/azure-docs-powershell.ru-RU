---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210644"
---
# <span data-ttu-id="1f643-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="1f643-101">Save-AzContext</span></span>

## <span data-ttu-id="1f643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f643-102">SYNOPSIS</span></span>
<span data-ttu-id="1f643-103">Сохранение текущих сведений проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1f643-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="1f643-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f643-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f643-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f643-105">DESCRIPTION</span></span>
<span data-ttu-id="1f643-106">С Save-AzContext-коды сохраняется текущая проверка подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1f643-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="1f643-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f643-107">EXAMPLES</span></span>

### <span data-ttu-id="1f643-108">Пример 1. Сохранение контекста текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="1f643-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="1f643-109">В этом примере контекст Azure текущего сеанса сохраняется в предоставленном файле JSON.</span><span class="sxs-lookup"><span data-stu-id="1f643-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="1f643-110">Пример 2. Сохранение заданного контекста</span><span class="sxs-lookup"><span data-stu-id="1f643-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="1f643-111">В этом примере сохраняется контекст Azure, переданный в cmdlet в предоставленный файл JSON.</span><span class="sxs-lookup"><span data-stu-id="1f643-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="1f643-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f643-112">PARAMETERS</span></span>

### <span data-ttu-id="1f643-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f643-113">-DefaultProfile</span></span>
<span data-ttu-id="1f643-114">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f643-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f643-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1f643-115">-Force</span></span>
<span data-ttu-id="1f643-116">Переописывать файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="1f643-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="1f643-117">-Path</span><span class="sxs-lookup"><span data-stu-id="1f643-117">-Path</span></span>
<span data-ttu-id="1f643-118">Путь к файлу, в который нужно сохранить данные проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1f643-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="1f643-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="1f643-119">-Profile</span></span>
<span data-ttu-id="1f643-120">Определяет контекст Azure, из которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f643-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="1f643-121">Если не указать контекст, этот cmdlet будет читать текст из локального контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f643-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="1f643-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f643-122">-Confirm</span></span>
<span data-ttu-id="1f643-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f643-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f643-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f643-124">-WhatIf</span></span>
<span data-ttu-id="1f643-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f643-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f643-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f643-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f643-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f643-127">CommonParameters</span></span>
<span data-ttu-id="1f643-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f643-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f643-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f643-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f643-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f643-130">INPUTS</span></span>

### <span data-ttu-id="1f643-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="1f643-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="1f643-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f643-132">OUTPUTS</span></span>

### <span data-ttu-id="1f643-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="1f643-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="1f643-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f643-134">NOTES</span></span>

## <span data-ttu-id="1f643-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f643-135">RELATED LINKS</span></span>
