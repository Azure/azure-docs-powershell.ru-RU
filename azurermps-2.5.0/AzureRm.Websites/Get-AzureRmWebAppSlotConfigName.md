---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: ff05a30c495475b63b0385f3398c78e0b018a4bc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914346"
---
# <span data-ttu-id="702af-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="702af-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="702af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="702af-102">SYNOPSIS</span></span>
<span data-ttu-id="702af-103">Получение списка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="702af-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="702af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="702af-104">SYNTAX</span></span>

### <span data-ttu-id="702af-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="702af-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="702af-106">S2</span><span class="sxs-lookup"><span data-stu-id="702af-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="702af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="702af-107">DESCRIPTION</span></span>
<span data-ttu-id="702af-108">Командлет **Get-AzureRmWebAppSlotConfigName** извлекает список параметров приложения и имен строк подключения, которые в настоящее время помечены как параметры слота.</span><span class="sxs-lookup"><span data-stu-id="702af-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="702af-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="702af-109">EXAMPLES</span></span>

### <span data-ttu-id="702af-110">1:</span><span class="sxs-lookup"><span data-stu-id="702af-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="702af-111">Эта команда получает параметры приложения и строки соединения, относящиеся к веб-приложению ContosoSite, связанному с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="702af-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="702af-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="702af-112">PARAMETERS</span></span>

### <span data-ttu-id="702af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="702af-113">-DefaultProfile</span></span>
<span data-ttu-id="702af-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="702af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="702af-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="702af-115">-Name</span></span>
<span data-ttu-id="702af-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="702af-116">WebApp Name</span></span>

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

### <span data-ttu-id="702af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="702af-117">-ResourceGroupName</span></span>
<span data-ttu-id="702af-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="702af-118">Resource Group Name</span></span>

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

### <span data-ttu-id="702af-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="702af-119">-WebApp</span></span>
<span data-ttu-id="702af-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="702af-120">WebApp Object</span></span>

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

### <span data-ttu-id="702af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="702af-121">CommonParameters</span></span>
<span data-ttu-id="702af-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="702af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="702af-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="702af-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="702af-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="702af-124">INPUTS</span></span>

### <span data-ttu-id="702af-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="702af-125">Site</span></span>
<span data-ttu-id="702af-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="702af-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="702af-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="702af-127">OUTPUTS</span></span>

## <span data-ttu-id="702af-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="702af-128">NOTES</span></span>

## <span data-ttu-id="702af-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="702af-129">RELATED LINKS</span></span>

