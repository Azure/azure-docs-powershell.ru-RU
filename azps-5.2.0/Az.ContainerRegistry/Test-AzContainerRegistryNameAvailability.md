---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402799"
---
# <span data-ttu-id="8f7ad-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8f7ad-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="8f7ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7ad-103">Проверяет доступность имени контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="8f7ad-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="8f7ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f7ad-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f7ad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f7ad-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7ad-106">Этот Test-AzContainerRegistryNameAvailability проверяет, допустимо ли имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="8f7ad-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="8f7ad-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f7ad-107">EXAMPLES</span></span>

### <span data-ttu-id="8f7ad-108">Пример 1. Проверка доступности имени контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="8f7ad-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="8f7ad-109">Эта команда проверяет доступность имени контейнера в реестре \` SomeRegistryName. \`</span><span class="sxs-lookup"><span data-stu-id="8f7ad-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="8f7ad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f7ad-110">PARAMETERS</span></span>

### <span data-ttu-id="8f7ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7ad-111">-DefaultProfile</span></span>
<span data-ttu-id="8f7ad-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8f7ad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f7ad-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8f7ad-113">-Name</span></span>
<span data-ttu-id="8f7ad-114">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="8f7ad-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="8f7ad-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7ad-115">CommonParameters</span></span>
<span data-ttu-id="8f7ad-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7ad-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7ad-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f7ad-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7ad-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f7ad-118">INPUTS</span></span>

### <span data-ttu-id="8f7ad-119">System.String</span><span class="sxs-lookup"><span data-stu-id="8f7ad-119">System.String</span></span>

## <span data-ttu-id="8f7ad-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f7ad-120">OUTPUTS</span></span>

### <span data-ttu-id="8f7ad-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="8f7ad-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="8f7ad-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f7ad-122">NOTES</span></span>

## <span data-ttu-id="8f7ad-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f7ad-123">RELATED LINKS</span></span>

[<span data-ttu-id="8f7ad-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8f7ad-124">New-AzContainerRegistry</span></span>]()

