---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076471"
---
# <span data-ttu-id="da830-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="da830-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="da830-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da830-102">SYNOPSIS</span></span>
<span data-ttu-id="da830-103">Удаляет указанную учетную запись служб мультимедиа Azure.</span><span class="sxs-lookup"><span data-stu-id="da830-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="da830-104">**Примечание.**  Эта версия устарела, ознакомьтесь с [более новой версией](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="da830-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="da830-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da830-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da830-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da830-106">DESCRIPTION</span></span>
<span data-ttu-id="da830-107">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="da830-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="da830-108">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="da830-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="da830-109">Командлет **Remove-AzureMediaServicesAccount** удаляет учетную запись служб мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="da830-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="da830-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da830-110">EXAMPLES</span></span>

### <span data-ttu-id="da830-111">Пример 1: Удаление учетной записи служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="da830-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="da830-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da830-112">PARAMETERS</span></span>

### <span data-ttu-id="da830-113">-Force</span><span class="sxs-lookup"><span data-stu-id="da830-113">-Force</span></span>
<span data-ttu-id="da830-114">Если указан параметр *Force* , удаление не подтверждено.</span><span class="sxs-lookup"><span data-stu-id="da830-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="da830-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da830-115">-Name</span></span>
<span data-ttu-id="da830-116">Имя учетной записи службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="da830-116">The Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da830-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="da830-117">-Profile</span></span>
<span data-ttu-id="da830-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="da830-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da830-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da830-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da830-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da830-120">-Confirm</span></span>
<span data-ttu-id="da830-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da830-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da830-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da830-122">-WhatIf</span></span>
<span data-ttu-id="da830-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da830-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da830-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da830-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da830-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da830-125">CommonParameters</span></span>
<span data-ttu-id="da830-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da830-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da830-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da830-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da830-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da830-128">INPUTS</span></span>

## <span data-ttu-id="da830-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da830-129">OUTPUTS</span></span>

## <span data-ttu-id="da830-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="da830-130">NOTES</span></span>

## <span data-ttu-id="da830-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da830-131">RELATED LINKS</span></span>

[<span data-ttu-id="da830-132">Использование Azure PowerShell для служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="da830-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="da830-133">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="da830-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="da830-134">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="da830-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)


