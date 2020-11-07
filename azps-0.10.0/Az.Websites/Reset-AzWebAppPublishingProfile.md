---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 519a072a0c51f489a78992e483dec8aa9cd1fab5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910583"
---
# <span data-ttu-id="3e2e4-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="3e2e4-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="3e2e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e2e4-102">SYNOPSIS</span></span>

## <span data-ttu-id="3e2e4-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e2e4-103">SYNTAX</span></span>

### <span data-ttu-id="3e2e4-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="3e2e4-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e2e4-105">S2</span><span class="sxs-lookup"><span data-stu-id="3e2e4-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e2e4-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e2e4-106">DESCRIPTION</span></span>
<span data-ttu-id="3e2e4-107">Командлет **Reset-AzWebAppPublishingProfile** сбрасывает профиль публикации для указанного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="3e2e4-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="3e2e4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e2e4-108">EXAMPLES</span></span>

### <span data-ttu-id="3e2e4-109">1:</span><span class="sxs-lookup"><span data-stu-id="3e2e4-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="3e2e4-110">Эта команда сбрасывает профиль публикации для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="3e2e4-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3e2e4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e2e4-111">PARAMETERS</span></span>

### <span data-ttu-id="3e2e4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2e4-112">-DefaultProfile</span></span>
<span data-ttu-id="3e2e4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e2e4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2e4-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e2e4-114">-Name</span></span>
<span data-ttu-id="3e2e4-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="3e2e4-115">WebApp Name</span></span>

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

### <span data-ttu-id="3e2e4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e2e4-116">-ResourceGroupName</span></span>
<span data-ttu-id="3e2e4-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3e2e4-117">Resource Group Name</span></span>

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

### <span data-ttu-id="3e2e4-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3e2e4-118">-WebApp</span></span>
<span data-ttu-id="3e2e4-119">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="3e2e4-119">WebApp Object</span></span>

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

### <span data-ttu-id="3e2e4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2e4-120">CommonParameters</span></span>
<span data-ttu-id="3e2e4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e2e4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2e4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e2e4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2e4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e2e4-123">INPUTS</span></span>

### <span data-ttu-id="3e2e4-124">Семейств</span><span class="sxs-lookup"><span data-stu-id="3e2e4-124">Site</span></span>
<span data-ttu-id="3e2e4-125">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3e2e4-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3e2e4-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e2e4-126">OUTPUTS</span></span>

## <span data-ttu-id="3e2e4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e2e4-127">NOTES</span></span>

## <span data-ttu-id="3e2e4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e2e4-128">RELATED LINKS</span></span>

