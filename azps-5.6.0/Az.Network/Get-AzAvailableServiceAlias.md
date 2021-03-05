---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 4eb210380feaaf101bad45b4bd0b4df26533f9e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993894"
---
# <span data-ttu-id="8a7c0-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="8a7c0-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="8a7c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7c0-103">Получите доступные псевдонимы служб в регионе.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="8a7c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a7c0-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a7c0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a7c0-105">DESCRIPTION</span></span>
<span data-ttu-id="8a7c0-106">Для получения всех доступных псевдонимов службы в предоставленном расположении можно использовать все псевдонимы службы **Get-AzAvailableServiceAlias.**</span><span class="sxs-lookup"><span data-stu-id="8a7c0-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="8a7c0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a7c0-107">EXAMPLES</span></span>

### <span data-ttu-id="8a7c0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a7c0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="8a7c0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a7c0-109">PARAMETERS</span></span>

### <span data-ttu-id="8a7c0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a7c0-110">-DefaultProfile</span></span>
<span data-ttu-id="8a7c0-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a7c0-112">-Location</span><span class="sxs-lookup"><span data-stu-id="8a7c0-112">-Location</span></span>
<span data-ttu-id="8a7c0-113">Расположение.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-113">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a7c0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7c0-114">CommonParameters</span></span>
<span data-ttu-id="8a7c0-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7c0-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a7c0-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7c0-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a7c0-117">INPUTS</span></span>

### <span data-ttu-id="8a7c0-118">System.String</span><span class="sxs-lookup"><span data-stu-id="8a7c0-118">System.String</span></span>

## <span data-ttu-id="8a7c0-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a7c0-119">OUTPUTS</span></span>

### <span data-ttu-id="8a7c0-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="8a7c0-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="8a7c0-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a7c0-121">NOTES</span></span>

## <span data-ttu-id="8a7c0-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a7c0-122">RELATED LINKS</span></span>
