---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 414e25840b03127bbe94586248641e103c1f7d88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910608"
---
# <span data-ttu-id="93bd7-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="93bd7-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="93bd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="93bd7-103">Получение списка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="93bd7-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="93bd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93bd7-104">SYNTAX</span></span>

### <span data-ttu-id="93bd7-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="93bd7-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93bd7-106">S2</span><span class="sxs-lookup"><span data-stu-id="93bd7-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93bd7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93bd7-107">DESCRIPTION</span></span>
<span data-ttu-id="93bd7-108">Командлет **Get-AzWebAppSlotConfigName** извлекает список параметров приложения и имен строк подключения, которые в настоящее время помечены как параметры слота.</span><span class="sxs-lookup"><span data-stu-id="93bd7-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="93bd7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93bd7-109">EXAMPLES</span></span>

### <span data-ttu-id="93bd7-110">1:</span><span class="sxs-lookup"><span data-stu-id="93bd7-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="93bd7-111">Эта команда получает параметры приложения и строки соединения, относящиеся к веб-приложению ContosoSite, связанному с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="93bd7-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="93bd7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93bd7-112">PARAMETERS</span></span>

### <span data-ttu-id="93bd7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bd7-113">-DefaultProfile</span></span>
<span data-ttu-id="93bd7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93bd7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93bd7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93bd7-115">-Name</span></span>
<span data-ttu-id="93bd7-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="93bd7-116">WebApp Name</span></span>

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

### <span data-ttu-id="93bd7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93bd7-117">-ResourceGroupName</span></span>
<span data-ttu-id="93bd7-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="93bd7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="93bd7-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="93bd7-119">-WebApp</span></span>
<span data-ttu-id="93bd7-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="93bd7-120">WebApp Object</span></span>

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

### <span data-ttu-id="93bd7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bd7-121">CommonParameters</span></span>
<span data-ttu-id="93bd7-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93bd7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bd7-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93bd7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bd7-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93bd7-124">INPUTS</span></span>

### <span data-ttu-id="93bd7-125">Семейств</span><span class="sxs-lookup"><span data-stu-id="93bd7-125">Site</span></span>
<span data-ttu-id="93bd7-126">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="93bd7-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="93bd7-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93bd7-127">OUTPUTS</span></span>

## <span data-ttu-id="93bd7-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="93bd7-128">NOTES</span></span>

## <span data-ttu-id="93bd7-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93bd7-129">RELATED LINKS</span></span>

