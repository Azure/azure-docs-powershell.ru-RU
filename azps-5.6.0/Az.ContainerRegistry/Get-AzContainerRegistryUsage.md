---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 7a950bc3b375ea9d86ef71eda120ac1d92fbd8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990349"
---
# <span data-ttu-id="75d8b-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="75d8b-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="75d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="75d8b-103">Получить использование реестра контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="75d8b-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="75d8b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75d8b-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d8b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="75d8b-106">Получить использование реестра контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="75d8b-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="75d8b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="75d8b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75d8b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="75d8b-109">Получить использование реестра контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="75d8b-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="75d8b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75d8b-110">PARAMETERS</span></span>

### <span data-ttu-id="75d8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d8b-111">-DefaultProfile</span></span>
<span data-ttu-id="75d8b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75d8b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d8b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="75d8b-113">-Name</span></span>
<span data-ttu-id="75d8b-114">Имя целевого реестра.</span><span class="sxs-lookup"><span data-stu-id="75d8b-114">Target registry name.</span></span>

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

### <span data-ttu-id="75d8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="75d8b-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d8b-116">Resource group name.</span></span>

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

### <span data-ttu-id="75d8b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d8b-117">CommonParameters</span></span>
<span data-ttu-id="75d8b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d8b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d8b-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75d8b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d8b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75d8b-120">INPUTS</span></span>

### <span data-ttu-id="75d8b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="75d8b-121">System.String</span></span>

## <span data-ttu-id="75d8b-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75d8b-122">OUTPUTS</span></span>

### <span data-ttu-id="75d8b-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="75d8b-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="75d8b-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75d8b-124">NOTES</span></span>

## <span data-ttu-id="75d8b-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75d8b-125">RELATED LINKS</span></span>
