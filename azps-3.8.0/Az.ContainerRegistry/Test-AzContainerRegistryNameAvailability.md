---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912057"
---
# <span data-ttu-id="a8bf6-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a8bf6-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="a8bf6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bf6-103">Проверяет доступность имени контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="a8bf6-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="a8bf6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8bf6-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8bf6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="a8bf6-106">Командлет Test-AzContainerRegistryNameAvailability проверяет, является ли имя реестра контейнера допустимым и доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="a8bf6-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="a8bf6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="a8bf6-108">Пример 1: Проверка доступности имени контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="a8bf6-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="a8bf6-109">Эта команда проверяет доступность имени контейнера в реестре \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="a8bf6-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="a8bf6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8bf6-110">PARAMETERS</span></span>

### <span data-ttu-id="a8bf6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bf6-111">-DefaultProfile</span></span>
<span data-ttu-id="a8bf6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8bf6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8bf6-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a8bf6-113">-Name</span></span>
<span data-ttu-id="a8bf6-114">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="a8bf6-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="a8bf6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bf6-115">CommonParameters</span></span>
<span data-ttu-id="a8bf6-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8bf6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bf6-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8bf6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bf6-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8bf6-118">INPUTS</span></span>

### <span data-ttu-id="a8bf6-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a8bf6-119">System.String</span></span>

## <span data-ttu-id="a8bf6-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8bf6-120">OUTPUTS</span></span>

### <span data-ttu-id="a8bf6-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="a8bf6-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="a8bf6-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8bf6-122">NOTES</span></span>

## <span data-ttu-id="a8bf6-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8bf6-123">RELATED LINKS</span></span>

[<span data-ttu-id="a8bf6-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a8bf6-124">New-AzContainerRegistry</span></span>]()

