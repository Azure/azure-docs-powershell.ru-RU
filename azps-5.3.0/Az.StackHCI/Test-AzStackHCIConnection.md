---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418924"
---
# <span data-ttu-id="c7181-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="c7181-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="c7181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7181-102">SYNOPSIS</span></span>
<span data-ttu-id="c7181-103">Test-AzStackHCIConnection проверяет подключение из локального узла с кластером к службам Azure, которые требуются azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="c7181-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="c7181-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7181-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="c7181-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7181-105">DESCRIPTION</span></span>
<span data-ttu-id="c7181-106">Test-AzStackHCIConnection проверяет подключение из локального узла с кластером к службам Azure, которые требуются azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="c7181-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="c7181-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7181-107">EXAMPLES</span></span>

### <span data-ttu-id="c7181-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="c7181-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="c7181-109">C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span><span class="sxs-lookup"><span data-stu-id="c7181-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="c7181-110">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="c7181-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="c7181-111">C:\PS \> Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="c7181-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="c7181-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7181-112">PARAMETERS</span></span>

### <span data-ttu-id="c7181-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="c7181-113">-ComputerName</span></span>
<span data-ttu-id="c7181-114">Указывает один из узлов кластера в локальном кластере, регистрируется в Azure.</span><span class="sxs-lookup"><span data-stu-id="c7181-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7181-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="c7181-115">-Credential</span></span>
<span data-ttu-id="c7181-116">Определяет учетные данные для computerName.</span><span class="sxs-lookup"><span data-stu-id="c7181-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="c7181-117">По умолчанию выполняется текущий пользователь, который выполняет cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7181-117">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7181-118">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="c7181-118">-EnvironmentName</span></span>
<span data-ttu-id="c7181-119">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="c7181-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="c7181-120">По умолчанию это AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="c7181-120">Default is AzureCloud.</span></span>
<span data-ttu-id="c7181-121">Допустимые значения: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="c7181-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7181-122">-Регион</span><span class="sxs-lookup"><span data-stu-id="c7181-122">-Region</span></span>
<span data-ttu-id="c7181-123">Определяет регион, к который нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="c7181-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="c7181-124">Используется, если только это не является canary region.</span><span class="sxs-lookup"><span data-stu-id="c7181-124">Not used unless it is Canary region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7181-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7181-125">CommonParameters</span></span>
<span data-ttu-id="c7181-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7181-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7181-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7181-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7181-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7181-128">INPUTS</span></span>

## <span data-ttu-id="c7181-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7181-129">OUTPUTS</span></span>

### <span data-ttu-id="c7181-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="c7181-130">PSCustomObject.</span></span> <span data-ttu-id="c7181-131">Возвращает следующие свойства в PSCustomObject:</span><span class="sxs-lookup"><span data-stu-id="c7181-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="c7181-132">Проверка: имя выполненного теста.</span><span class="sxs-lookup"><span data-stu-id="c7181-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="c7181-133">Конечная точкаТест: используемая в тесте конечная точка.</span><span class="sxs-lookup"><span data-stu-id="c7181-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="c7181-134">IsRequired: True или False</span><span class="sxs-lookup"><span data-stu-id="c7181-134">IsRequired: True or False</span></span>
### <span data-ttu-id="c7181-135">Результат: "Успешно" или "Сбой"</span><span class="sxs-lookup"><span data-stu-id="c7181-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="c7181-136">FailedNodes: список узлов, на которых не удалось проверить.</span><span class="sxs-lookup"><span data-stu-id="c7181-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="c7181-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7181-137">NOTES</span></span>

## <span data-ttu-id="c7181-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7181-138">RELATED LINKS</span></span>
