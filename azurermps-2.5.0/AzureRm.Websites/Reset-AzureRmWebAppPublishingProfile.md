---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: f082241be9e31b11782fcbbf5570a7f3c3947012
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913252"
---
# <span data-ttu-id="8a308-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="8a308-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="8a308-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a308-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a308-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a308-103">SYNTAX</span></span>

### <span data-ttu-id="8a308-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="8a308-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a308-105">S2</span><span class="sxs-lookup"><span data-stu-id="8a308-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a308-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a308-106">DESCRIPTION</span></span>
<span data-ttu-id="8a308-107">Командлет **Reset-AzureRmWebAppPublishingProfile** сбрасывает профиль публикации для указанного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="8a308-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="8a308-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a308-108">EXAMPLES</span></span>

### <span data-ttu-id="8a308-109">1:</span><span class="sxs-lookup"><span data-stu-id="8a308-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="8a308-110">Эта команда сбрасывает профиль публикации для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8a308-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8a308-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a308-111">PARAMETERS</span></span>

### <span data-ttu-id="8a308-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a308-112">-DefaultProfile</span></span>
<span data-ttu-id="8a308-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a308-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a308-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a308-114">-Name</span></span>
<span data-ttu-id="8a308-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="8a308-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a308-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a308-116">-ResourceGroupName</span></span>
<span data-ttu-id="8a308-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8a308-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a308-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8a308-118">-WebApp</span></span>
<span data-ttu-id="8a308-119">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="8a308-119">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a308-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a308-120">CommonParameters</span></span>
<span data-ttu-id="8a308-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a308-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a308-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a308-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a308-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a308-123">INPUTS</span></span>

### <span data-ttu-id="8a308-124">Семейств</span><span class="sxs-lookup"><span data-stu-id="8a308-124">Site</span></span>
<span data-ttu-id="8a308-125">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8a308-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8a308-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a308-126">OUTPUTS</span></span>

## <span data-ttu-id="8a308-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a308-127">NOTES</span></span>

## <span data-ttu-id="8a308-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a308-128">RELATED LINKS</span></span>

