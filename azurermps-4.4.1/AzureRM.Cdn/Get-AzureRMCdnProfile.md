---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: 726e84e1fe43e90ebf16241a017dadb2af5584b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568329"
---
# <span data-ttu-id="07e0d-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="07e0d-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="07e0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="07e0d-103">Получает профиль CDN.</span><span class="sxs-lookup"><span data-stu-id="07e0d-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07e0d-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07e0d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07e0d-105">DESCRIPTION</span></span>
<span data-ttu-id="07e0d-106">Командлет **Get-AzureRMCdnProfile** получает профиль сети доставки содержимого (CDN) для Azure и связанную с ней информацию.</span><span class="sxs-lookup"><span data-stu-id="07e0d-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="07e0d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07e0d-107">EXAMPLES</span></span>

## <span data-ttu-id="07e0d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07e0d-108">PARAMETERS</span></span>

### <span data-ttu-id="07e0d-109">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="07e0d-109">-ProfileName</span></span>
<span data-ttu-id="07e0d-110">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="07e0d-110">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e0d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e0d-111">-ResourceGroupName</span></span>
<span data-ttu-id="07e0d-112">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="07e0d-112">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e0d-113">-DefaultProfile</span></span>
<span data-ttu-id="07e0d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07e0d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07e0d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e0d-115">CommonParameters</span></span>
<span data-ttu-id="07e0d-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07e0d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e0d-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e0d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e0d-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07e0d-118">INPUTS</span></span>

## <span data-ttu-id="07e0d-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07e0d-119">OUTPUTS</span></span>

###  
<span data-ttu-id="07e0d-120">Этот командлет возвращает объект профиля.</span><span class="sxs-lookup"><span data-stu-id="07e0d-120">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="07e0d-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="07e0d-121">NOTES</span></span>

## <span data-ttu-id="07e0d-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07e0d-122">RELATED LINKS</span></span>

[<span data-ttu-id="07e0d-123">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="07e0d-123">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="07e0d-124">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="07e0d-124">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="07e0d-125">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="07e0d-125">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


