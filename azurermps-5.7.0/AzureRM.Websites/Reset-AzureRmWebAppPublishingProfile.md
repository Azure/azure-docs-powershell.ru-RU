---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: b519012104472d9b97f5f0a5e4b699829b99fff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567857"
---
# <span data-ttu-id="745c2-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="745c2-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="745c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="745c2-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="745c2-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="745c2-103">SYNTAX</span></span>

### <span data-ttu-id="745c2-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="745c2-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="745c2-105">S2</span><span class="sxs-lookup"><span data-stu-id="745c2-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="745c2-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="745c2-106">DESCRIPTION</span></span>
<span data-ttu-id="745c2-107">Командлет **Reset-AzureRmWebAppPublishingProfile** сбрасывает профиль публикации для указанного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="745c2-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="745c2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="745c2-108">EXAMPLES</span></span>

### <span data-ttu-id="745c2-109">1:</span><span class="sxs-lookup"><span data-stu-id="745c2-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="745c2-110">Эта команда сбрасывает профиль публикации для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="745c2-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="745c2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="745c2-111">PARAMETERS</span></span>

### <span data-ttu-id="745c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745c2-112">-DefaultProfile</span></span>
<span data-ttu-id="745c2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="745c2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="745c2-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="745c2-114">-Name</span></span>
<span data-ttu-id="745c2-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="745c2-115">WebApp Name</span></span>

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

### <span data-ttu-id="745c2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="745c2-116">-ResourceGroupName</span></span>
<span data-ttu-id="745c2-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="745c2-117">Resource Group Name</span></span>

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

### <span data-ttu-id="745c2-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="745c2-118">-WebApp</span></span>
<span data-ttu-id="745c2-119">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="745c2-119">WebApp Object</span></span>

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

### <span data-ttu-id="745c2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745c2-120">CommonParameters</span></span>
<span data-ttu-id="745c2-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="745c2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745c2-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="745c2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745c2-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="745c2-123">INPUTS</span></span>

### <span data-ttu-id="745c2-124">Семейств</span><span class="sxs-lookup"><span data-stu-id="745c2-124">Site</span></span>
<span data-ttu-id="745c2-125">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="745c2-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="745c2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="745c2-126">OUTPUTS</span></span>

## <span data-ttu-id="745c2-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="745c2-127">NOTES</span></span>

## <span data-ttu-id="745c2-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="745c2-128">RELATED LINKS</span></span>

