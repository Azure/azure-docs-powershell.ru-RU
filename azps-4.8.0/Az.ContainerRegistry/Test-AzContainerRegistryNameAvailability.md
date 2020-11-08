---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236458"
---
# <span data-ttu-id="1d4c9-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1d4c9-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="1d4c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4c9-103">Проверяет доступность имени контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="1d4c9-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="1d4c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d4c9-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d4c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d4c9-105">DESCRIPTION</span></span>
<span data-ttu-id="1d4c9-106">Командлет Test-AzContainerRegistryNameAvailability проверяет, является ли имя реестра контейнера допустимым и доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="1d4c9-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="1d4c9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d4c9-107">EXAMPLES</span></span>

### <span data-ttu-id="1d4c9-108">Пример 1: Проверка доступности имени контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="1d4c9-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="1d4c9-109">Эта команда проверяет доступность имени контейнера в реестре \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="1d4c9-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="1d4c9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d4c9-110">PARAMETERS</span></span>

### <span data-ttu-id="1d4c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4c9-111">-DefaultProfile</span></span>
<span data-ttu-id="1d4c9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d4c9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d4c9-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d4c9-113">-Name</span></span>
<span data-ttu-id="1d4c9-114">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="1d4c9-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="1d4c9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4c9-115">CommonParameters</span></span>
<span data-ttu-id="1d4c9-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d4c9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4c9-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d4c9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4c9-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d4c9-118">INPUTS</span></span>

### <span data-ttu-id="1d4c9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1d4c9-119">System.String</span></span>

## <span data-ttu-id="1d4c9-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d4c9-120">OUTPUTS</span></span>

### <span data-ttu-id="1d4c9-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="1d4c9-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="1d4c9-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d4c9-122">NOTES</span></span>

## <span data-ttu-id="1d4c9-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d4c9-123">RELATED LINKS</span></span>

[<span data-ttu-id="1d4c9-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1d4c9-124">New-AzContainerRegistry</span></span>]()

