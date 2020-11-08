---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 691d8cf006e720d706d2473f76ff8660927e73ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245582"
---
# <span data-ttu-id="d6540-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="d6540-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="d6540-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6540-102">SYNOPSIS</span></span>
<span data-ttu-id="d6540-103">Получение сведений об использовании реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="d6540-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="d6540-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6540-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6540-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6540-105">DESCRIPTION</span></span>
<span data-ttu-id="d6540-106">Получение сведений об использовании реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="d6540-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="d6540-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6540-107">EXAMPLES</span></span>

### <span data-ttu-id="d6540-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6540-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="d6540-109">Получение сведений об использовании реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="d6540-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="d6540-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6540-110">PARAMETERS</span></span>

### <span data-ttu-id="d6540-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6540-111">-DefaultProfile</span></span>
<span data-ttu-id="d6540-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6540-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6540-113">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d6540-113">-RegistryName</span></span>
<span data-ttu-id="d6540-114">Целевое имя реестра.</span><span class="sxs-lookup"><span data-stu-id="d6540-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6540-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6540-115">-ResourceGroupName</span></span>
<span data-ttu-id="d6540-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6540-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6540-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6540-117">CommonParameters</span></span>
<span data-ttu-id="d6540-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6540-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6540-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6540-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6540-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6540-120">INPUTS</span></span>

### <span data-ttu-id="d6540-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d6540-121">System.String</span></span>

## <span data-ttu-id="d6540-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6540-122">OUTPUTS</span></span>

### <span data-ttu-id="d6540-123">Microsoft. Azure. Commands. ContainerRegistry. Models. PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="d6540-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="d6540-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6540-124">NOTES</span></span>

## <span data-ttu-id="d6540-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6540-125">RELATED LINKS</span></span>
