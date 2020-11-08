---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242918"
---
# <span data-ttu-id="d6f24-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="d6f24-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="d6f24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6f24-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f24-103">Сброс указанного ключа доступа.</span><span class="sxs-lookup"><span data-stu-id="d6f24-103">Resets the specified access key.</span></span>

## <span data-ttu-id="d6f24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6f24-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f24-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6f24-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f24-106">Командлет **Reset-AzPowerBIWorkspaceCollectionAccessKey** сбрасывает указанный ключ доступа в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="d6f24-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="d6f24-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6f24-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f24-108">Пример 1: сброс первичной клавиши доступа</span><span class="sxs-lookup"><span data-stu-id="d6f24-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="d6f24-109">Эта команда сбрасывает первичный ключ доступа для коллекции рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6f24-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="d6f24-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6f24-110">PARAMETERS</span></span>

### <span data-ttu-id="d6f24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f24-111">-DefaultProfile</span></span>
<span data-ttu-id="d6f24-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d6f24-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6f24-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="d6f24-113">-Key1</span></span>
<span data-ttu-id="d6f24-114">Указывает на то, что этот командлет сбрасывает первичную клавишу доступа.</span><span class="sxs-lookup"><span data-stu-id="d6f24-114">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f24-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="d6f24-115">-Key2</span></span>
<span data-ttu-id="d6f24-116">Указывает на то, что этот командлет сбрасывает вторичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="d6f24-116">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f24-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f24-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6f24-118">Указывает имя группы ресурсов коллекции.</span><span class="sxs-lookup"><span data-stu-id="d6f24-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="d6f24-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="d6f24-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="d6f24-120">Указывает имя коллекции рабочих областей Power BI, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d6f24-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f24-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6f24-121">-Confirm</span></span>
<span data-ttu-id="d6f24-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6f24-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f24-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f24-123">-WhatIf</span></span>
<span data-ttu-id="d6f24-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6f24-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f24-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6f24-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f24-126">CommonParameters</span></span>
<span data-ttu-id="d6f24-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6f24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f24-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f24-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f24-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6f24-129">INPUTS</span></span>

### <span data-ttu-id="d6f24-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d6f24-130">System.String</span></span>

## <span data-ttu-id="d6f24-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6f24-131">OUTPUTS</span></span>

### <span data-ttu-id="d6f24-132">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="d6f24-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="d6f24-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6f24-133">NOTES</span></span>

## <span data-ttu-id="d6f24-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6f24-134">RELATED LINKS</span></span>

[<span data-ttu-id="d6f24-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="d6f24-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


