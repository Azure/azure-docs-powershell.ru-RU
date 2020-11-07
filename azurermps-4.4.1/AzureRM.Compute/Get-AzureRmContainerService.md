---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: 3bdb0a0f497f6e7a6ebff4b4d449e75fa759f7a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734577"
---
# <span data-ttu-id="3fa02-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3fa02-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="3fa02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fa02-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa02-103">Возвращает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="3fa02-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fa02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fa02-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fa02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fa02-105">DESCRIPTION</span></span>
<span data-ttu-id="3fa02-106">Командлет **Get-AzureRmContainerService** Получает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="3fa02-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="3fa02-107">Вы можете просматривать свойства службы контейнеров, в том числе состояние, количество основных и агентов, а также полное доменное имя главного и агента.</span><span class="sxs-lookup"><span data-stu-id="3fa02-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="3fa02-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fa02-108">EXAMPLES</span></span>

### <span data-ttu-id="3fa02-109">Пример 1: получение службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="3fa02-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="3fa02-110">Эта команда получает службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="3fa02-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="3fa02-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fa02-111">PARAMETERS</span></span>

### <span data-ttu-id="3fa02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa02-112">-DefaultProfile</span></span>
<span data-ttu-id="3fa02-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa02-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fa02-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3fa02-114">-Name</span></span>
<span data-ttu-id="3fa02-115">Указывает имя службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3fa02-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa02-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa02-116">-ResourceGroupName</span></span>
<span data-ttu-id="3fa02-117">Указывает группу ресурсов для службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3fa02-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa02-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa02-118">CommonParameters</span></span>
<span data-ttu-id="3fa02-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fa02-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa02-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa02-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa02-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fa02-121">INPUTS</span></span>

## <span data-ttu-id="3fa02-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fa02-122">OUTPUTS</span></span>

## <span data-ttu-id="3fa02-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fa02-123">NOTES</span></span>

## <span data-ttu-id="3fa02-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fa02-124">RELATED LINKS</span></span>

[<span data-ttu-id="3fa02-125">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3fa02-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="3fa02-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3fa02-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="3fa02-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3fa02-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


