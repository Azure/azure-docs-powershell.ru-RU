---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239928"
---
# <span data-ttu-id="37751-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="37751-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="37751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37751-102">SYNOPSIS</span></span>
<span data-ttu-id="37751-103">Проверяет наличие экземпляра сервера Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="37751-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="37751-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37751-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37751-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37751-105">DESCRIPTION</span></span>
<span data-ttu-id="37751-106">Этот Test-AzAnalysisServicesServer проверяет наличие экземпляра сервера Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="37751-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="37751-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37751-107">EXAMPLES</span></span>

### <span data-ttu-id="37751-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37751-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="37751-109">Эта команда проверяется, есть ли сервер с именем testerver в тестовой группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="37751-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="37751-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37751-110">PARAMETERS</span></span>

### <span data-ttu-id="37751-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37751-111">-DefaultProfile</span></span>
<span data-ttu-id="37751-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37751-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37751-113">-Name</span><span class="sxs-lookup"><span data-stu-id="37751-113">-Name</span></span>
<span data-ttu-id="37751-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="37751-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37751-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37751-115">-ResourceGroupName</span></span>
<span data-ttu-id="37751-116">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="37751-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="37751-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37751-117">CommonParameters</span></span>
<span data-ttu-id="37751-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37751-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37751-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37751-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37751-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37751-120">INPUTS</span></span>

### <span data-ttu-id="37751-121">System.String</span><span class="sxs-lookup"><span data-stu-id="37751-121">System.String</span></span>

## <span data-ttu-id="37751-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37751-122">OUTPUTS</span></span>

### <span data-ttu-id="37751-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37751-123">System.Boolean</span></span>

## <span data-ttu-id="37751-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37751-124">NOTES</span></span>
<span data-ttu-id="37751-125">Псевдоним: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="37751-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="37751-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37751-126">RELATED LINKS</span></span>

[<span data-ttu-id="37751-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="37751-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="37751-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="37751-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
