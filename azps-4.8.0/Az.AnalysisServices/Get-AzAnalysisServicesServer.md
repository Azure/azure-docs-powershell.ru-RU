---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242677"
---
# <span data-ttu-id="659ea-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="659ea-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="659ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="659ea-102">SYNOPSIS</span></span>
<span data-ttu-id="659ea-103">Получает сведения о сервере служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="659ea-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="659ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="659ea-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="659ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="659ea-105">DESCRIPTION</span></span>
<span data-ttu-id="659ea-106">Командлет Get-AzAnalysisServicesServer получает сведения о сервере служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="659ea-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="659ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="659ea-107">EXAMPLES</span></span>

### <span data-ttu-id="659ea-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="659ea-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="659ea-109">Эта команда получает все серверы служб аналитики Azure в группе ресурсов с именем ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="659ea-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="659ea-110">Пример 2: получение сервера</span><span class="sxs-lookup"><span data-stu-id="659ea-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="659ea-111">Эта команда получает сервер служб аналитики Azure с именем TestServer в группе ресурсов с именем ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="659ea-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="659ea-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="659ea-112">PARAMETERS</span></span>

### <span data-ttu-id="659ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="659ea-113">-DefaultProfile</span></span>
<span data-ttu-id="659ea-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="659ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="659ea-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="659ea-115">-Name</span></span>
<span data-ttu-id="659ea-116">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="659ea-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="659ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="659ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="659ea-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="659ea-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="659ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="659ea-119">CommonParameters</span></span>
<span data-ttu-id="659ea-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="659ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="659ea-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="659ea-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="659ea-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="659ea-122">INPUTS</span></span>

### <span data-ttu-id="659ea-123">System. String</span><span class="sxs-lookup"><span data-stu-id="659ea-123">System.String</span></span>

## <span data-ttu-id="659ea-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="659ea-124">OUTPUTS</span></span>

### <span data-ttu-id="659ea-125">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="659ea-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="659ea-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="659ea-126">NOTES</span></span>
<span data-ttu-id="659ea-127">Alias (псевдоним): Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="659ea-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="659ea-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="659ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="659ea-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="659ea-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="659ea-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="659ea-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)