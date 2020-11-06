---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: a345b69fdc6695706f61a85c2926392c9f522aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559279"
---
# <span data-ttu-id="73744-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="73744-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="73744-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73744-102">SYNOPSIS</span></span>
<span data-ttu-id="73744-103">Получает профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="73744-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73744-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73744-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73744-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73744-105">DESCRIPTION</span></span>
<span data-ttu-id="73744-106">Командлет **Get-AzureRMCdnProfile** получает профиль сети доставки содержимого (CDN) для Azure и связанную с ней информацию.</span><span class="sxs-lookup"><span data-stu-id="73744-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="73744-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73744-107">EXAMPLES</span></span>

## <span data-ttu-id="73744-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73744-108">PARAMETERS</span></span>

### <span data-ttu-id="73744-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73744-109">-DefaultProfile</span></span>
<span data-ttu-id="73744-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="73744-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73744-111">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="73744-111">-ProfileName</span></span>
<span data-ttu-id="73744-112">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="73744-112">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73744-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73744-113">-ResourceGroupName</span></span>
<span data-ttu-id="73744-114">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="73744-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73744-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73744-115">CommonParameters</span></span>
<span data-ttu-id="73744-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73744-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73744-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73744-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73744-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73744-118">INPUTS</span></span>

### <span data-ttu-id="73744-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="73744-119">None</span></span>
<span data-ttu-id="73744-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="73744-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73744-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73744-121">OUTPUTS</span></span>

###  
<span data-ttu-id="73744-122">Этот командлет возвращает объект профиля.</span><span class="sxs-lookup"><span data-stu-id="73744-122">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="73744-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="73744-123">NOTES</span></span>

## <span data-ttu-id="73744-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73744-124">RELATED LINKS</span></span>

[<span data-ttu-id="73744-125">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="73744-125">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="73744-126">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="73744-126">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="73744-127">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="73744-127">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


