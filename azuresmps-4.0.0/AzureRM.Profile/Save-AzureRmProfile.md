---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555784"
---
# <span data-ttu-id="4d599-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="4d599-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="4d599-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d599-102">SYNOPSIS</span></span>
<span data-ttu-id="4d599-103">Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d599-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="4d599-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d599-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d599-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d599-105">DESCRIPTION</span></span>
<span data-ttu-id="4d599-106">Командлет Save-AzureRmProfile сохраняет текущие сведения для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d599-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="4d599-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d599-107">EXAMPLES</span></span>

### <span data-ttu-id="4d599-108">Пример 1: сохранение профиля текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="4d599-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="4d599-109">В этом примере профиль Azure текущего сеанса сохраняется в указанном JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="4d599-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="4d599-110">Пример 2: сохранение определенного профиля</span><span class="sxs-lookup"><span data-stu-id="4d599-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="4d599-111">В этом примере выполняется сохранение профиля Azure, который передается в командлет, в указанный файл JSON.</span><span class="sxs-lookup"><span data-stu-id="4d599-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="4d599-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d599-112">PARAMETERS</span></span>

### <span data-ttu-id="4d599-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4d599-113">-Force</span></span>
<span data-ttu-id="4d599-114">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="4d599-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="4d599-115">-Path</span><span class="sxs-lookup"><span data-stu-id="4d599-115">-Path</span></span>
<span data-ttu-id="4d599-116">Задает путь к файлу, в который нужно сохранить сведения для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4d599-116">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="4d599-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="4d599-117">-Profile</span></span>
<span data-ttu-id="4d599-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4d599-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4d599-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d599-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d599-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d599-120">-Confirm</span></span>
<span data-ttu-id="4d599-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d599-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d599-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d599-122">-WhatIf</span></span>
<span data-ttu-id="4d599-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d599-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d599-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d599-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d599-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d599-125">CommonParameters</span></span>
<span data-ttu-id="4d599-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d599-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d599-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d599-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d599-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d599-128">INPUTS</span></span>

## <span data-ttu-id="4d599-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d599-129">OUTPUTS</span></span>

### <span data-ttu-id="4d599-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="4d599-130">PSAzureProfile</span></span>

## <span data-ttu-id="4d599-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d599-131">NOTES</span></span>

## <span data-ttu-id="4d599-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d599-132">RELATED LINKS</span></span>

[<span data-ttu-id="4d599-133">SELECT-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="4d599-133">Select-AzureRMProfile</span></span>]()

