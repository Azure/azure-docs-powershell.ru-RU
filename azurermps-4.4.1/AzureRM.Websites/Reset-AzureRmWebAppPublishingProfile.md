---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: f1224ae7ad95598d8ae947d0e38ef3a9cf7a4dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560415"
---
# <span data-ttu-id="d84f8-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="d84f8-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="d84f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d84f8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d84f8-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d84f8-103">SYNTAX</span></span>

### <span data-ttu-id="d84f8-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="d84f8-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d84f8-105">S2</span><span class="sxs-lookup"><span data-stu-id="d84f8-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d84f8-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d84f8-106">DESCRIPTION</span></span>
<span data-ttu-id="d84f8-107">Командлет **Reset-AzureRmWebAppPublishingProfile** сбрасывает профиль публикации для указанного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d84f8-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="d84f8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d84f8-108">EXAMPLES</span></span>

### <span data-ttu-id="d84f8-109">1:</span><span class="sxs-lookup"><span data-stu-id="d84f8-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="d84f8-110">Эта команда сбрасывает профиль публикации для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d84f8-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d84f8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d84f8-111">PARAMETERS</span></span>

### <span data-ttu-id="d84f8-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d84f8-112">-Name</span></span>
<span data-ttu-id="d84f8-113">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="d84f8-113">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84f8-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84f8-114">-ResourceGroupName</span></span>
<span data-ttu-id="d84f8-115">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d84f8-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84f8-116">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d84f8-116">-WebApp</span></span>
<span data-ttu-id="d84f8-117">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="d84f8-117">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d84f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84f8-118">-DefaultProfile</span></span>
<span data-ttu-id="d84f8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d84f8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d84f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84f8-120">CommonParameters</span></span>
<span data-ttu-id="d84f8-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d84f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84f8-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84f8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84f8-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d84f8-123">INPUTS</span></span>

### <span data-ttu-id="d84f8-124">Семейств</span><span class="sxs-lookup"><span data-stu-id="d84f8-124">Site</span></span>
<span data-ttu-id="d84f8-125">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d84f8-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d84f8-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d84f8-126">OUTPUTS</span></span>

## <span data-ttu-id="d84f8-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d84f8-127">NOTES</span></span>

## <span data-ttu-id="d84f8-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d84f8-128">RELATED LINKS</span></span>

