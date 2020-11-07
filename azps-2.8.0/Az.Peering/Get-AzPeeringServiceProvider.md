---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 786a8009d1423b6b12fae4d7eb8da6899a8cd108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904617"
---
# <span data-ttu-id="82b8e-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="82b8e-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="82b8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="82b8e-103">Получает список поставщиков услуг пиринга, сопоставленных с корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="82b8e-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="82b8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82b8e-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b8e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b8e-105">DESCRIPTION</span></span>
<span data-ttu-id="82b8e-106">Список поставщиков служб пиринга</span><span class="sxs-lookup"><span data-stu-id="82b8e-106">List peering service providers</span></span>

## <span data-ttu-id="82b8e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82b8e-107">EXAMPLES</span></span>

### <span data-ttu-id="82b8e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82b8e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="82b8e-109">Получение доступа к службам пиринга</span><span class="sxs-lookup"><span data-stu-id="82b8e-109">Gets available peering service providers</span></span>

## <span data-ttu-id="82b8e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82b8e-110">PARAMETERS</span></span>

### <span data-ttu-id="82b8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b8e-111">-DefaultProfile</span></span>
<span data-ttu-id="82b8e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82b8e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b8e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b8e-113">CommonParameters</span></span>
<span data-ttu-id="82b8e-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82b8e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b8e-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82b8e-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b8e-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82b8e-116">INPUTS</span></span>

### <span data-ttu-id="82b8e-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="82b8e-117">None</span></span>

## <span data-ttu-id="82b8e-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b8e-118">OUTPUTS</span></span>

### <span data-ttu-id="82b8e-119">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServiceProvider)</span><span class="sxs-lookup"><span data-stu-id="82b8e-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="82b8e-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="82b8e-120">NOTES</span></span>

## <span data-ttu-id="82b8e-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82b8e-121">RELATED LINKS</span></span>
