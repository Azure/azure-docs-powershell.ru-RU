---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 23a5fa01424d62796fec331213ffebb43121cec0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911940"
---
# <span data-ttu-id="11694-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="11694-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="11694-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11694-102">SYNOPSIS</span></span>
<span data-ttu-id="11694-103">Получить доступные псевдонимы служб в регионе.</span><span class="sxs-lookup"><span data-stu-id="11694-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="11694-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11694-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11694-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11694-105">DESCRIPTION</span></span>
<span data-ttu-id="11694-106">Командлет **Get-AzAvailableServiceAlias** позволяет получить все доступные псевдонимы служб для подсети в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="11694-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="11694-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11694-107">EXAMPLES</span></span>

### <span data-ttu-id="11694-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11694-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAliases -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="11694-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11694-109">PARAMETERS</span></span>

### <span data-ttu-id="11694-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11694-110">-DefaultProfile</span></span>
<span data-ttu-id="11694-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11694-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11694-112">-Location</span><span class="sxs-lookup"><span data-stu-id="11694-112">-Location</span></span>
<span data-ttu-id="11694-113">Расположение.</span><span class="sxs-lookup"><span data-stu-id="11694-113">The location.</span></span>

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

### <span data-ttu-id="11694-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11694-114">CommonParameters</span></span>
<span data-ttu-id="11694-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11694-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11694-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11694-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11694-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11694-117">INPUTS</span></span>

### <span data-ttu-id="11694-118">System. String</span><span class="sxs-lookup"><span data-stu-id="11694-118">System.String</span></span>

## <span data-ttu-id="11694-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11694-119">OUTPUTS</span></span>

### <span data-ttu-id="11694-120">Microsoft. Azure. Commands. Network. Models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="11694-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="11694-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="11694-121">NOTES</span></span>

## <span data-ttu-id="11694-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11694-122">RELATED LINKS</span></span>
