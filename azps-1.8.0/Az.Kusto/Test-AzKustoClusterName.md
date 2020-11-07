---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: 9a3d8397914317d733c8da47e7d095e1acb541e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900014"
---
# <span data-ttu-id="63da0-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="63da0-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="63da0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63da0-102">SYNOPSIS</span></span>
<span data-ttu-id="63da0-103">Убедитесь в том, что данное имя кластера Kusto доступно.</span><span class="sxs-lookup"><span data-stu-id="63da0-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="63da0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63da0-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63da0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63da0-105">DESCRIPTION</span></span>
<span data-ttu-id="63da0-106">Убедитесь в том, что данное имя кластера Kusto доступно.</span><span class="sxs-lookup"><span data-stu-id="63da0-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="63da0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63da0-107">EXAMPLES</span></span>

### <span data-ttu-id="63da0-108">Пример 1: Проверка доступности используемого имени кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="63da0-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="63da0-109">Указанная выше команда возвращает значение, указывающее, существует ли кластер Kusto с именем "mykustocluster" в регионе "Центральная американская".</span><span class="sxs-lookup"><span data-stu-id="63da0-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="63da0-110">Пример 2: Проверка доступности неиспользуемого имени кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="63da0-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="63da0-111">Указанная выше команда возвращает значение, указывающее, существует ли кластер Kusto с именем "mykustocluster" в регионе "Центральная американская".</span><span class="sxs-lookup"><span data-stu-id="63da0-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="63da0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63da0-112">PARAMETERS</span></span>

### <span data-ttu-id="63da0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63da0-113">-DefaultProfile</span></span>
<span data-ttu-id="63da0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63da0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63da0-115">-Location</span><span class="sxs-lookup"><span data-stu-id="63da0-115">-Location</span></span>
<span data-ttu-id="63da0-116">Расположение для проверки.</span><span class="sxs-lookup"><span data-stu-id="63da0-116">The location where to check.</span></span>

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

### <span data-ttu-id="63da0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63da0-117">-Name</span></span>
<span data-ttu-id="63da0-118">Имя определенного кластера.</span><span class="sxs-lookup"><span data-stu-id="63da0-118">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="63da0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63da0-119">CommonParameters</span></span>
<span data-ttu-id="63da0-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63da0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63da0-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63da0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63da0-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63da0-122">INPUTS</span></span>

### <span data-ttu-id="63da0-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="63da0-123">None</span></span>

## <span data-ttu-id="63da0-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63da0-124">OUTPUTS</span></span>

### <span data-ttu-id="63da0-125">Microsoft. Azure. Commands. Kusto. Models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="63da0-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="63da0-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="63da0-126">NOTES</span></span>

## <span data-ttu-id="63da0-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63da0-127">RELATED LINKS</span></span>
