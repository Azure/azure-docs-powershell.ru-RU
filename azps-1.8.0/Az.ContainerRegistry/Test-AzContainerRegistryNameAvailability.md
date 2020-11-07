---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 4471835a1ff87a44722fc9e0dd51b0fa279410f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901030"
---
# <span data-ttu-id="bf99f-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="bf99f-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="bf99f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf99f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf99f-103">Проверяет доступность имени контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="bf99f-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="bf99f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf99f-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf99f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf99f-105">DESCRIPTION</span></span>
<span data-ttu-id="bf99f-106">Командлет Test-AzContainerRegistryNameAvailability проверяет, является ли имя реестра контейнера допустимым и доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="bf99f-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="bf99f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf99f-107">EXAMPLES</span></span>

### <span data-ttu-id="bf99f-108">Пример 1: Проверка доступности имени контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="bf99f-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="bf99f-109">Эта команда проверяет доступность имени контейнера в реестре \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="bf99f-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="bf99f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf99f-110">PARAMETERS</span></span>

### <span data-ttu-id="bf99f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf99f-111">-DefaultProfile</span></span>
<span data-ttu-id="bf99f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bf99f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf99f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf99f-113">-Name</span></span>
<span data-ttu-id="bf99f-114">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="bf99f-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="bf99f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf99f-115">CommonParameters</span></span>
<span data-ttu-id="bf99f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf99f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf99f-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf99f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf99f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf99f-118">INPUTS</span></span>

### <span data-ttu-id="bf99f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="bf99f-119">System.String</span></span>

## <span data-ttu-id="bf99f-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf99f-120">OUTPUTS</span></span>

### <span data-ttu-id="bf99f-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="bf99f-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="bf99f-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf99f-122">NOTES</span></span>

## <span data-ttu-id="bf99f-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf99f-123">RELATED LINKS</span></span>

[<span data-ttu-id="bf99f-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bf99f-124">New-AzContainerRegistry</span></span>]()

