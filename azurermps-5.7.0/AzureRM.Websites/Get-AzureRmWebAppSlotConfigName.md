---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 96e9c5945938addfbd629ef66b5f68e54c0427e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561315"
---
# <span data-ttu-id="e36b1-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="e36b1-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="e36b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e36b1-102">SYNOPSIS</span></span>
<span data-ttu-id="e36b1-103">Получение списка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="e36b1-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e36b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e36b1-104">SYNTAX</span></span>

### <span data-ttu-id="e36b1-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="e36b1-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e36b1-106">S2</span><span class="sxs-lookup"><span data-stu-id="e36b1-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e36b1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e36b1-107">DESCRIPTION</span></span>
<span data-ttu-id="e36b1-108">Командлет **Get-AzureRmWebAppSlotConfigName** извлекает список параметров приложения и имен строк подключения, которые в настоящее время помечены как параметры слота.</span><span class="sxs-lookup"><span data-stu-id="e36b1-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="e36b1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e36b1-109">EXAMPLES</span></span>

### <span data-ttu-id="e36b1-110">1:</span><span class="sxs-lookup"><span data-stu-id="e36b1-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e36b1-111">Эта команда получает параметры приложения и строки соединения, относящиеся к веб-приложению ContosoSite, связанному с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="e36b1-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e36b1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e36b1-112">PARAMETERS</span></span>

### <span data-ttu-id="e36b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36b1-113">-DefaultProfile</span></span>
<span data-ttu-id="e36b1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e36b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e36b1-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e36b1-115">-Name</span></span>
<span data-ttu-id="e36b1-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="e36b1-116">WebApp Name</span></span>

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

### <span data-ttu-id="e36b1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36b1-117">-ResourceGroupName</span></span>
<span data-ttu-id="e36b1-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e36b1-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e36b1-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e36b1-119">-WebApp</span></span>
<span data-ttu-id="e36b1-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="e36b1-120">WebApp Object</span></span>

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

### <span data-ttu-id="e36b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36b1-121">CommonParameters</span></span>
<span data-ttu-id="e36b1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e36b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36b1-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36b1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36b1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e36b1-124">INPUTS</span></span>

### <span data-ttu-id="e36b1-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="e36b1-125">Site</span></span>
<span data-ttu-id="e36b1-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e36b1-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e36b1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e36b1-127">OUTPUTS</span></span>

## <span data-ttu-id="e36b1-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e36b1-128">NOTES</span></span>

## <span data-ttu-id="e36b1-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e36b1-129">RELATED LINKS</span></span>

