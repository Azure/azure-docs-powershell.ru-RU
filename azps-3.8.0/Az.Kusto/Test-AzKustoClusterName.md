---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: c6b2f462ac66ab48b50e7555a3b5bf7c844aae3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065585"
---
# <span data-ttu-id="376b9-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="376b9-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="376b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="376b9-102">SYNOPSIS</span></span>
<span data-ttu-id="376b9-103">Убедитесь в том, что данное имя кластера Kusto доступно.</span><span class="sxs-lookup"><span data-stu-id="376b9-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="376b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="376b9-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="376b9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="376b9-105">DESCRIPTION</span></span>
<span data-ttu-id="376b9-106">Убедитесь в том, что данное имя кластера Kusto доступно.</span><span class="sxs-lookup"><span data-stu-id="376b9-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="376b9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="376b9-107">EXAMPLES</span></span>

### <span data-ttu-id="376b9-108">Пример 1: Проверка доступности используемого имени кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="376b9-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="376b9-109">Указанная выше команда возвращает значение, указывающее, существует ли кластер Kusto с именем "mykustocluster" в регионе "Центральная американская".</span><span class="sxs-lookup"><span data-stu-id="376b9-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="376b9-110">Пример 2: Проверка доступности неиспользуемого имени кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="376b9-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="376b9-111">Указанная выше команда возвращает значение, указывающее, существует ли кластер Kusto с именем "mykustocluster" в регионе "Центральная американская".</span><span class="sxs-lookup"><span data-stu-id="376b9-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="376b9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="376b9-112">PARAMETERS</span></span>

### <span data-ttu-id="376b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376b9-113">-DefaultProfile</span></span>
<span data-ttu-id="376b9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="376b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="376b9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="376b9-115">-Location</span></span>
<span data-ttu-id="376b9-116">Расположение для проверки.</span><span class="sxs-lookup"><span data-stu-id="376b9-116">The location where to check.</span></span>

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

### <span data-ttu-id="376b9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="376b9-117">-Name</span></span>
<span data-ttu-id="376b9-118">Имя определенного кластера.</span><span class="sxs-lookup"><span data-stu-id="376b9-118">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="376b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376b9-119">CommonParameters</span></span>
<span data-ttu-id="376b9-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="376b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376b9-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376b9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376b9-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="376b9-122">INPUTS</span></span>

### <span data-ttu-id="376b9-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="376b9-123">None</span></span>

## <span data-ttu-id="376b9-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="376b9-124">OUTPUTS</span></span>

### <span data-ttu-id="376b9-125">Microsoft. Azure. Commands. Kusto. Models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="376b9-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="376b9-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="376b9-126">NOTES</span></span>

## <span data-ttu-id="376b9-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="376b9-127">RELATED LINKS</span></span>
