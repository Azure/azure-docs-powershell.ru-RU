---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: e7d84439b2292d70604f3f7d9e827a0d8cc035e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519399"
---
# <span data-ttu-id="ab8b7-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ab8b7-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="ab8b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8b7-103">Получить использование реестра контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8b7-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ab8b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab8b7-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab8b7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab8b7-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8b7-106">Получить использование реестра контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8b7-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ab8b7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab8b7-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8b7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab8b7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="ab8b7-109">Получить использование реестра контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8b7-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ab8b7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab8b7-110">PARAMETERS</span></span>

### <span data-ttu-id="ab8b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8b7-111">-DefaultProfile</span></span>
<span data-ttu-id="ab8b7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8b7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab8b7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ab8b7-113">-Name</span></span>
<span data-ttu-id="ab8b7-114">Имя целевого реестра.</span><span class="sxs-lookup"><span data-stu-id="ab8b7-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8b7-115">-ResourceGroupName</span></span>
<span data-ttu-id="ab8b7-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab8b7-116">Resource group name.</span></span>

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

### <span data-ttu-id="ab8b7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8b7-117">CommonParameters</span></span>
<span data-ttu-id="ab8b7-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8b7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8b7-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab8b7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8b7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab8b7-120">INPUTS</span></span>

### <span data-ttu-id="ab8b7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ab8b7-121">System.String</span></span>

## <span data-ttu-id="ab8b7-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab8b7-122">OUTPUTS</span></span>

### <span data-ttu-id="ab8b7-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ab8b7-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="ab8b7-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab8b7-124">NOTES</span></span>

## <span data-ttu-id="ab8b7-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab8b7-125">RELATED LINKS</span></span>
