---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: ec0b95ffee67d5597a06ed0729cded33e7489465
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910582"
---
# <span data-ttu-id="bdb08-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="bdb08-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="bdb08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdb08-102">SYNOPSIS</span></span>

## <span data-ttu-id="bdb08-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdb08-103">SYNTAX</span></span>

### <span data-ttu-id="bdb08-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="bdb08-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdb08-105">S2</span><span class="sxs-lookup"><span data-stu-id="bdb08-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdb08-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdb08-106">DESCRIPTION</span></span>
<span data-ttu-id="bdb08-107">Командлет **Reset-AzWebAppSlotPublishingProfile** сбрасывает профиль публикации для указанной области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="bdb08-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="bdb08-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdb08-108">EXAMPLES</span></span>

### <span data-ttu-id="bdb08-109">1:</span><span class="sxs-lookup"><span data-stu-id="bdb08-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="bdb08-110">Эта команда сбрасывает профиль публикации для слота с именем slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="bdb08-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="bdb08-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdb08-111">PARAMETERS</span></span>

### <span data-ttu-id="bdb08-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb08-112">-DefaultProfile</span></span>
<span data-ttu-id="bdb08-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdb08-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdb08-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bdb08-114">-Name</span></span>
<span data-ttu-id="bdb08-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="bdb08-115">WebApp Name</span></span>

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

### <span data-ttu-id="bdb08-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb08-116">-ResourceGroupName</span></span>
<span data-ttu-id="bdb08-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bdb08-117">Resource Group Name</span></span>

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

### <span data-ttu-id="bdb08-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="bdb08-118">-Slot</span></span>
<span data-ttu-id="bdb08-119">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="bdb08-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb08-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bdb08-120">-WebApp</span></span>
<span data-ttu-id="bdb08-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="bdb08-121">WebApp Object</span></span>

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

### <span data-ttu-id="bdb08-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb08-122">CommonParameters</span></span>
<span data-ttu-id="bdb08-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdb08-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb08-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb08-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb08-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdb08-125">INPUTS</span></span>

### <span data-ttu-id="bdb08-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="bdb08-126">Site</span></span>
<span data-ttu-id="bdb08-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bdb08-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bdb08-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdb08-128">OUTPUTS</span></span>

## <span data-ttu-id="bdb08-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdb08-129">NOTES</span></span>

## <span data-ttu-id="bdb08-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdb08-130">RELATED LINKS</span></span>

