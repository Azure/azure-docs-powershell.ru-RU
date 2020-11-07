---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: c377beb022b3d44d8b96a560c4bdd8b0c6daa387
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734542"
---
# <span data-ttu-id="6a352-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6a352-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="6a352-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a352-102">SYNOPSIS</span></span>
<span data-ttu-id="6a352-103">Удаляет набор рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="6a352-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a352-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a352-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a352-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a352-105">DESCRIPTION</span></span>
<span data-ttu-id="6a352-106">Командлет **Remove-AzureRmPowerBIWorkspaceCollection** удаляет набор рабочих областей Power BI из подписки на Azure и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a352-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="6a352-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a352-107">EXAMPLES</span></span>

### <span data-ttu-id="6a352-108">Пример 1: Удаление коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="6a352-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="6a352-109">Эта команда удаляет набор рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a352-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="6a352-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a352-110">PARAMETERS</span></span>

### <span data-ttu-id="6a352-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a352-111">-ResourceGroupName</span></span>
<span data-ttu-id="6a352-112">Указывает имя группы ресурсов, из которой этот командлет удаляет коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="6a352-112">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="6a352-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="6a352-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="6a352-114">Указывает имя коллекции рабочих областей Power BI, которую этот командлет удаляет.</span><span class="sxs-lookup"><span data-stu-id="6a352-114">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a352-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a352-115">-Confirm</span></span>
<span data-ttu-id="6a352-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a352-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a352-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a352-117">-WhatIf</span></span>
<span data-ttu-id="6a352-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a352-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a352-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a352-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a352-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a352-120">-DefaultProfile</span></span>
<span data-ttu-id="6a352-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a352-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a352-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a352-122">CommonParameters</span></span>
<span data-ttu-id="6a352-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a352-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a352-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a352-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a352-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a352-125">INPUTS</span></span>

## <span data-ttu-id="6a352-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a352-126">OUTPUTS</span></span>

## <span data-ttu-id="6a352-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a352-127">NOTES</span></span>

## <span data-ttu-id="6a352-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a352-128">RELATED LINKS</span></span>

[<span data-ttu-id="6a352-129">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6a352-129">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="6a352-130">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="6a352-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


