---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: b6a01079bed80017054e7fe52673012827dce02d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557688"
---
# <span data-ttu-id="6a9f8-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="6a9f8-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="6a9f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a9f8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a9f8-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a9f8-103">SYNTAX</span></span>

### <span data-ttu-id="6a9f8-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="6a9f8-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9f8-105">S2</span><span class="sxs-lookup"><span data-stu-id="6a9f8-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a9f8-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a9f8-106">DESCRIPTION</span></span>
<span data-ttu-id="6a9f8-107">Командлет **Reset-AzureRmWebAppSlotPublishingProfile** сбрасывает профиль публикации для указанной области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="6a9f8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a9f8-108">EXAMPLES</span></span>

### <span data-ttu-id="6a9f8-109">1:</span><span class="sxs-lookup"><span data-stu-id="6a9f8-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="6a9f8-110">Эта команда сбрасывает профиль публикации для слота с именем slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6a9f8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a9f8-111">PARAMETERS</span></span>

### <span data-ttu-id="6a9f8-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6a9f8-112">-Name</span></span>
<span data-ttu-id="6a9f8-113">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="6a9f8-113">WebApp Name</span></span>

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

### <span data-ttu-id="6a9f8-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9f8-114">-ResourceGroupName</span></span>
<span data-ttu-id="6a9f8-115">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6a9f8-115">Resource Group Name</span></span>

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

### <span data-ttu-id="6a9f8-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="6a9f8-116">-Slot</span></span>
<span data-ttu-id="6a9f8-117">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="6a9f8-117">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9f8-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6a9f8-118">-WebApp</span></span>
<span data-ttu-id="6a9f8-119">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="6a9f8-119">WebApp Object</span></span>

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

### <span data-ttu-id="6a9f8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9f8-120">-DefaultProfile</span></span>
<span data-ttu-id="6a9f8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a9f8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9f8-122">CommonParameters</span></span>
<span data-ttu-id="6a9f8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9f8-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9f8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9f8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a9f8-125">INPUTS</span></span>

### <span data-ttu-id="6a9f8-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="6a9f8-126">Site</span></span>
<span data-ttu-id="6a9f8-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6a9f8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a9f8-128">OUTPUTS</span></span>

## <span data-ttu-id="6a9f8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a9f8-129">NOTES</span></span>

## <span data-ttu-id="6a9f8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a9f8-130">RELATED LINKS</span></span>

