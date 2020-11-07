---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: ad2a97895f4876c008d1740e962bb3b746e67ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734888"
---
# <span data-ttu-id="b76e6-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b76e6-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="b76e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b76e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b76e6-103">Проверяет доступность имени контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="b76e6-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b76e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b76e6-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b76e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b76e6-105">DESCRIPTION</span></span>
<span data-ttu-id="b76e6-106">Командлет **Test-AzureRmContainerRegistryNameAvailability** проверяет, является ли имя контейнера в реестре допустимым и доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="b76e6-106">The **Test-AzureRmContainerRegistryNameAvailability** cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="b76e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b76e6-107">EXAMPLES</span></span>

### <span data-ttu-id="b76e6-108">Пример 1: Проверка доступности имени контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="b76e6-108">Example 1: Check the availability of a container registry name</span></span>
```
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="b76e6-109">Эта команда проверяет доступность имени контейнера в реестре `SomeRegistryName` .</span><span class="sxs-lookup"><span data-stu-id="b76e6-109">This command checks the availability of the container registry name `SomeRegistryName`.</span></span>

## <span data-ttu-id="b76e6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b76e6-110">PARAMETERS</span></span>

### <span data-ttu-id="b76e6-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b76e6-111">-Name</span></span>
<span data-ttu-id="b76e6-112">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="b76e6-112">Container Registry Name.</span></span>

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

### <span data-ttu-id="b76e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76e6-113">-DefaultProfile</span></span>
<span data-ttu-id="b76e6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b76e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76e6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76e6-115">CommonParameters</span></span>
<span data-ttu-id="b76e6-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b76e6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76e6-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76e6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76e6-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b76e6-118">INPUTS</span></span>

## <span data-ttu-id="b76e6-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b76e6-119">OUTPUTS</span></span>

### <span data-ttu-id="b76e6-120">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="b76e6-120">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="b76e6-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="b76e6-121">NOTES</span></span>

## <span data-ttu-id="b76e6-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b76e6-122">RELATED LINKS</span></span>

[<span data-ttu-id="b76e6-123">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b76e6-123">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

