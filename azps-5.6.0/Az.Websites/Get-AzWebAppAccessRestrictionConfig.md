---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983832"
---
# <span data-ttu-id="12cd2-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="12cd2-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="12cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="12cd2-103">Получает конфигурацию рестикции Access для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="12cd2-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="12cd2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12cd2-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12cd2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="12cd2-106">Для этого с помощью **cmdlet Get-AzWebAppAccessRestrictionConfig** можно получить значение ограничения Access для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="12cd2-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="12cd2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="12cd2-108">Пример 1. Получить ограничение доступа к Веб-приложению из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="12cd2-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="12cd2-109">Эта команда получает ограничение доступа для веб-приложения ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="12cd2-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="12cd2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12cd2-110">PARAMETERS</span></span>

### <span data-ttu-id="12cd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cd2-111">-DefaultProfile</span></span>
<span data-ttu-id="12cd2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12cd2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12cd2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="12cd2-113">-Name</span></span>
<span data-ttu-id="12cd2-114">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="12cd2-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12cd2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12cd2-115">-ResourceGroupName</span></span>
<span data-ttu-id="12cd2-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="12cd2-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12cd2-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="12cd2-117">-SlotName</span></span>
<span data-ttu-id="12cd2-118">Название слота развертывания.</span><span class="sxs-lookup"><span data-stu-id="12cd2-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12cd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cd2-119">CommonParameters</span></span>
<span data-ttu-id="12cd2-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12cd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cd2-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12cd2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cd2-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12cd2-122">INPUTS</span></span>

### <span data-ttu-id="12cd2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="12cd2-123">System.String</span></span>

## <span data-ttu-id="12cd2-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12cd2-124">OUTPUTS</span></span>

### <span data-ttu-id="12cd2-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="12cd2-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="12cd2-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12cd2-126">NOTES</span></span>

## <span data-ttu-id="12cd2-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12cd2-127">RELATED LINKS</span></span>

[<span data-ttu-id="12cd2-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="12cd2-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="12cd2-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="12cd2-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="12cd2-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="12cd2-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
