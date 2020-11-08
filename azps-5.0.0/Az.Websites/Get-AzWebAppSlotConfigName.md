---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247129"
---
# <span data-ttu-id="77290-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="77290-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="77290-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77290-102">SYNOPSIS</span></span>
<span data-ttu-id="77290-103">Получение списка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="77290-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="77290-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77290-104">SYNTAX</span></span>

### <span data-ttu-id="77290-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="77290-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77290-106">S2</span><span class="sxs-lookup"><span data-stu-id="77290-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77290-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77290-107">DESCRIPTION</span></span>
<span data-ttu-id="77290-108">Командлет **Get-AzWebAppSlotConfigName** извлекает список параметров приложения и имен строк подключения, которые в настоящее время помечены как параметры слота.</span><span class="sxs-lookup"><span data-stu-id="77290-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="77290-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77290-109">EXAMPLES</span></span>

### <span data-ttu-id="77290-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77290-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="77290-111">Эта команда получает параметры приложения и строки соединения, относящиеся к веб-приложению ContosoSite, связанному с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="77290-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="77290-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77290-112">PARAMETERS</span></span>

### <span data-ttu-id="77290-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77290-113">-DefaultProfile</span></span>
<span data-ttu-id="77290-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77290-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77290-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="77290-115">-Name</span></span>
<span data-ttu-id="77290-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="77290-116">WebApp Name</span></span>

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

### <span data-ttu-id="77290-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77290-117">-ResourceGroupName</span></span>
<span data-ttu-id="77290-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="77290-118">Resource Group Name</span></span>

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

### <span data-ttu-id="77290-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="77290-119">-WebApp</span></span>
<span data-ttu-id="77290-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="77290-120">WebApp Object</span></span>

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

### <span data-ttu-id="77290-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77290-121">CommonParameters</span></span>
<span data-ttu-id="77290-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77290-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77290-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77290-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77290-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77290-124">INPUTS</span></span>

### <span data-ttu-id="77290-125">System. String</span><span class="sxs-lookup"><span data-stu-id="77290-125">System.String</span></span>

### <span data-ttu-id="77290-126">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="77290-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="77290-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77290-127">OUTPUTS</span></span>

### <span data-ttu-id="77290-128">Microsoft. Azure. Management. website. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="77290-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="77290-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="77290-129">NOTES</span></span>

## <span data-ttu-id="77290-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77290-130">RELATED LINKS</span></span>
