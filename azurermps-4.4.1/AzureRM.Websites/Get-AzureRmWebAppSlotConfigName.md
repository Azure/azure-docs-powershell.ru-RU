---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 196e653447204b65c7f431e29fe76078a268dda1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734503"
---
# <span data-ttu-id="99ade-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="99ade-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="99ade-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99ade-102">SYNOPSIS</span></span>
<span data-ttu-id="99ade-103">Получение списка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="99ade-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99ade-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99ade-104">SYNTAX</span></span>

### <span data-ttu-id="99ade-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="99ade-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99ade-106">S2</span><span class="sxs-lookup"><span data-stu-id="99ade-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99ade-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99ade-107">DESCRIPTION</span></span>
<span data-ttu-id="99ade-108">Командлет **Get-AzureRmWebAppSlotConfigName** извлекает список параметров приложения и имен строк подключения, которые в настоящее время помечены как параметры слота.</span><span class="sxs-lookup"><span data-stu-id="99ade-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="99ade-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99ade-109">EXAMPLES</span></span>

### <span data-ttu-id="99ade-110">1:</span><span class="sxs-lookup"><span data-stu-id="99ade-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="99ade-111">Эта команда получает параметры приложения и строки соединения, относящиеся к веб-приложению ContosoSite, связанному с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="99ade-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="99ade-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99ade-112">PARAMETERS</span></span>

### <span data-ttu-id="99ade-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99ade-113">-Name</span></span>
<span data-ttu-id="99ade-114">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="99ade-114">WebApp Name</span></span>

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

### <span data-ttu-id="99ade-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ade-115">-ResourceGroupName</span></span>
<span data-ttu-id="99ade-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="99ade-116">Resource Group Name</span></span>

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

### <span data-ttu-id="99ade-117">-WebApp</span><span class="sxs-lookup"><span data-stu-id="99ade-117">-WebApp</span></span>
<span data-ttu-id="99ade-118">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="99ade-118">WebApp Object</span></span>

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

### <span data-ttu-id="99ade-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ade-119">-DefaultProfile</span></span>
<span data-ttu-id="99ade-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99ade-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99ade-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ade-121">CommonParameters</span></span>
<span data-ttu-id="99ade-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99ade-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ade-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99ade-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ade-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99ade-124">INPUTS</span></span>

### <span data-ttu-id="99ade-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="99ade-125">Site</span></span>
<span data-ttu-id="99ade-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="99ade-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="99ade-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99ade-127">OUTPUTS</span></span>

## <span data-ttu-id="99ade-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="99ade-128">NOTES</span></span>

## <span data-ttu-id="99ade-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99ade-129">RELATED LINKS</span></span>

