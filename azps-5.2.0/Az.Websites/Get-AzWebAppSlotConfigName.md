---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392447"
---
# <span data-ttu-id="8b775-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="8b775-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="8b775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b775-102">SYNOPSIS</span></span>
<span data-ttu-id="8b775-103">Получить список имен веб-приложений slot Config</span><span class="sxs-lookup"><span data-stu-id="8b775-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="8b775-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b775-104">SYNTAX</span></span>

### <span data-ttu-id="8b775-105">S1</span><span class="sxs-lookup"><span data-stu-id="8b775-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b775-106">S2</span><span class="sxs-lookup"><span data-stu-id="8b775-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b775-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b775-107">DESCRIPTION</span></span>
<span data-ttu-id="8b775-108">С **помощью cmdlet Get-AzWebAppSlotConfigName** извлекает список имен "Параметры приложения" и "Строка подключения", которые в настоящее время помечены как параметры слота.</span><span class="sxs-lookup"><span data-stu-id="8b775-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="8b775-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b775-109">EXAMPLES</span></span>

### <span data-ttu-id="8b775-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b775-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8b775-111">Эта команда получает строки параметров приложения и подключения, относящиеся к веб-приложению ContosoSite, связанному с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8b775-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="8b775-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b775-112">PARAMETERS</span></span>

### <span data-ttu-id="8b775-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b775-113">-DefaultProfile</span></span>
<span data-ttu-id="8b775-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b775-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b775-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b775-115">-Name</span></span>
<span data-ttu-id="8b775-116">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="8b775-116">WebApp Name</span></span>

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

### <span data-ttu-id="8b775-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b775-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b775-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8b775-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8b775-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8b775-119">-WebApp</span></span>
<span data-ttu-id="8b775-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="8b775-120">WebApp Object</span></span>

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

### <span data-ttu-id="8b775-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b775-121">CommonParameters</span></span>
<span data-ttu-id="8b775-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b775-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b775-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b775-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b775-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b775-124">INPUTS</span></span>

### <span data-ttu-id="8b775-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8b775-125">System.String</span></span>

### <span data-ttu-id="8b775-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8b775-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8b775-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b775-127">OUTPUTS</span></span>

### <span data-ttu-id="8b775-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="8b775-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="8b775-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b775-129">NOTES</span></span>

## <span data-ttu-id="8b775-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b775-130">RELATED LINKS</span></span>
