---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076149"
---
# <span data-ttu-id="10e21-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="10e21-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="10e21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10e21-102">SYNOPSIS</span></span>
<span data-ttu-id="10e21-103">Удаляет изображение шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="10e21-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="10e21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10e21-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10e21-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10e21-105">DESCRIPTION</span></span>
<span data-ttu-id="10e21-106">Командлет **Remove-AzureRemoteAppTemplateImage** удаляет изображение шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="10e21-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="10e21-107">Изображение шаблона может быть удалено только в том случае, если оно не связано ни с одной коллекцией RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="10e21-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="10e21-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10e21-108">EXAMPLES</span></span>

### <span data-ttu-id="10e21-109">Пример 1: удаление изображения шаблона</span><span class="sxs-lookup"><span data-stu-id="10e21-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="10e21-110">Эта команда удаляет изображение шаблона с именем ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="10e21-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="10e21-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10e21-111">PARAMETERS</span></span>

### <span data-ttu-id="10e21-112">-ImageName</span><span class="sxs-lookup"><span data-stu-id="10e21-112">-ImageName</span></span>
<span data-ttu-id="10e21-113">Указывает имя образа шаблона RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="10e21-113">Specifies the name of the RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10e21-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="10e21-114">-Profile</span></span>
<span data-ttu-id="10e21-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10e21-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10e21-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10e21-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e21-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10e21-117">-Confirm</span></span>
<span data-ttu-id="10e21-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="10e21-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e21-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e21-119">-WhatIf</span></span>
<span data-ttu-id="10e21-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="10e21-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e21-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="10e21-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e21-122">CommonParameters</span></span>
<span data-ttu-id="10e21-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10e21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e21-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10e21-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e21-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10e21-125">INPUTS</span></span>

## <span data-ttu-id="10e21-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10e21-126">OUTPUTS</span></span>

## <span data-ttu-id="10e21-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="10e21-127">NOTES</span></span>

## <span data-ttu-id="10e21-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10e21-128">RELATED LINKS</span></span>

[<span data-ttu-id="10e21-129">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="10e21-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="10e21-130">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="10e21-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="10e21-131">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="10e21-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


