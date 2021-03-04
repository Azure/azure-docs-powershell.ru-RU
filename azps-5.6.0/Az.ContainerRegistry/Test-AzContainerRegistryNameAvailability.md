---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 0a0701a073101b0611f74a9443473fcd9568ca50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956339"
---
# <span data-ttu-id="75c7a-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="75c7a-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="75c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="75c7a-103">Проверяет доступность имени контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="75c7a-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="75c7a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75c7a-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75c7a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="75c7a-106">Этот Test-AzContainerRegistryNameAvailability проверяет, допустимо ли имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="75c7a-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="75c7a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75c7a-107">EXAMPLES</span></span>

### <span data-ttu-id="75c7a-108">Пример 1. Проверка доступности имени контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="75c7a-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="75c7a-109">Эта команда проверяет доступность имени контейнера в реестре \` SomeRegistryName. \`</span><span class="sxs-lookup"><span data-stu-id="75c7a-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="75c7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75c7a-110">PARAMETERS</span></span>

### <span data-ttu-id="75c7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c7a-111">-DefaultProfile</span></span>
<span data-ttu-id="75c7a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="75c7a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75c7a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="75c7a-113">-Name</span></span>
<span data-ttu-id="75c7a-114">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="75c7a-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75c7a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c7a-115">CommonParameters</span></span>
<span data-ttu-id="75c7a-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c7a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c7a-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75c7a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c7a-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75c7a-118">INPUTS</span></span>

### <span data-ttu-id="75c7a-119">System.String</span><span class="sxs-lookup"><span data-stu-id="75c7a-119">System.String</span></span>

## <span data-ttu-id="75c7a-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75c7a-120">OUTPUTS</span></span>

### <span data-ttu-id="75c7a-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="75c7a-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="75c7a-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75c7a-122">NOTES</span></span>

## <span data-ttu-id="75c7a-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75c7a-123">RELATED LINKS</span></span>

[<span data-ttu-id="75c7a-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="75c7a-124">New-AzContainerRegistry</span></span>]()

