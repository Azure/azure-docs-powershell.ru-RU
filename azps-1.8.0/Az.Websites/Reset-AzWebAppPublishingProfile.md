---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81eaa3b287a14cdc9aa71150c2f0b3724aeb4f4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728313"
---
# <span data-ttu-id="c5935-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c5935-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="c5935-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5935-102">SYNOPSIS</span></span>

## <span data-ttu-id="c5935-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5935-103">SYNTAX</span></span>

### <span data-ttu-id="c5935-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="c5935-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5935-105">S2</span><span class="sxs-lookup"><span data-stu-id="c5935-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5935-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5935-106">DESCRIPTION</span></span>
<span data-ttu-id="c5935-107">Командлет **Reset-AzWebAppPublishingProfile** сбрасывает профиль публикации для указанного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c5935-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="c5935-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5935-108">EXAMPLES</span></span>

### <span data-ttu-id="c5935-109">1:</span><span class="sxs-lookup"><span data-stu-id="c5935-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c5935-110">Эта команда сбрасывает профиль публикации для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c5935-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c5935-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5935-111">PARAMETERS</span></span>

### <span data-ttu-id="c5935-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5935-112">-DefaultProfile</span></span>
<span data-ttu-id="c5935-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5935-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5935-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5935-114">-Name</span></span>
<span data-ttu-id="c5935-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="c5935-115">WebApp Name</span></span>

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

### <span data-ttu-id="c5935-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5935-116">-ResourceGroupName</span></span>
<span data-ttu-id="c5935-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c5935-117">Resource Group Name</span></span>

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

### <span data-ttu-id="c5935-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c5935-118">-WebApp</span></span>
<span data-ttu-id="c5935-119">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="c5935-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5935-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5935-120">CommonParameters</span></span>
<span data-ttu-id="c5935-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5935-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5935-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5935-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5935-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5935-123">INPUTS</span></span>

### <span data-ttu-id="c5935-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c5935-124">System.String</span></span>

### <span data-ttu-id="c5935-125">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="c5935-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c5935-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5935-126">OUTPUTS</span></span>

### <span data-ttu-id="c5935-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c5935-127">System.String</span></span>

## <span data-ttu-id="c5935-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5935-128">NOTES</span></span>

## <span data-ttu-id="c5935-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5935-129">RELATED LINKS</span></span>
