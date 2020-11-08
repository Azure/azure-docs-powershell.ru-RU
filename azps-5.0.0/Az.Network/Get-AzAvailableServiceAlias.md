---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248133"
---
# <span data-ttu-id="9c071-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="9c071-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="9c071-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c071-102">SYNOPSIS</span></span>
<span data-ttu-id="9c071-103">Получить доступные псевдонимы служб в регионе.</span><span class="sxs-lookup"><span data-stu-id="9c071-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="9c071-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c071-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c071-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c071-105">DESCRIPTION</span></span>
<span data-ttu-id="9c071-106">Командлет **Get-AzAvailableServiceAlias** позволяет получить все доступные псевдонимы служб для подсети в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="9c071-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="9c071-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c071-107">EXAMPLES</span></span>

### <span data-ttu-id="9c071-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c071-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="9c071-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c071-109">PARAMETERS</span></span>

### <span data-ttu-id="9c071-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c071-110">-DefaultProfile</span></span>
<span data-ttu-id="9c071-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c071-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c071-112">-Location</span><span class="sxs-lookup"><span data-stu-id="9c071-112">-Location</span></span>
<span data-ttu-id="9c071-113">Расположение.</span><span class="sxs-lookup"><span data-stu-id="9c071-113">The location.</span></span>

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

### <span data-ttu-id="9c071-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c071-114">CommonParameters</span></span>
<span data-ttu-id="9c071-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c071-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c071-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c071-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c071-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c071-117">INPUTS</span></span>

### <span data-ttu-id="9c071-118">System. String</span><span class="sxs-lookup"><span data-stu-id="9c071-118">System.String</span></span>

## <span data-ttu-id="9c071-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c071-119">OUTPUTS</span></span>

### <span data-ttu-id="9c071-120">Microsoft. Azure. Commands. Network. Models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="9c071-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="9c071-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c071-121">NOTES</span></span>

## <span data-ttu-id="9c071-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c071-122">RELATED LINKS</span></span>
