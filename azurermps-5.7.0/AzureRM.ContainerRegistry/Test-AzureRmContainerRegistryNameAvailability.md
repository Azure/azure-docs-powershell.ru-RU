---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565535"
---
# <span data-ttu-id="bfb59-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="bfb59-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="bfb59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfb59-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb59-103">Проверяет доступность имени контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="bfb59-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfb59-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfb59-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfb59-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb59-106">Командлет Test-AzureRmContainerRegistryNameAvailability проверяет, является ли имя реестра контейнера допустимым и доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="bfb59-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="bfb59-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfb59-107">EXAMPLES</span></span>

### <span data-ttu-id="bfb59-108">Пример 1: Проверка доступности имени контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="bfb59-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="bfb59-109">Эта команда проверяет доступность имени контейнера в реестре \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="bfb59-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="bfb59-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfb59-110">PARAMETERS</span></span>

### <span data-ttu-id="bfb59-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfb59-111">-Name</span></span>
<span data-ttu-id="bfb59-112">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="bfb59-112">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb59-113">-DefaultProfile</span></span>
<span data-ttu-id="bfb59-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bfb59-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb59-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb59-115">CommonParameters</span></span>
<span data-ttu-id="bfb59-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfb59-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb59-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb59-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb59-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfb59-118">INPUTS</span></span>

### <span data-ttu-id="bfb59-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="bfb59-119">None</span></span>
<span data-ttu-id="bfb59-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bfb59-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfb59-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfb59-121">OUTPUTS</span></span>

### <span data-ttu-id="bfb59-122">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="bfb59-122">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="bfb59-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfb59-123">NOTES</span></span>

## <span data-ttu-id="bfb59-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfb59-124">RELATED LINKS</span></span>

[<span data-ttu-id="bfb59-125">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bfb59-125">New-AzureRmContainerRegistry</span></span>]()

