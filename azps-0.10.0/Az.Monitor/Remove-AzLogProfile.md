---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: c598b81990bd24d5808c48aa9511ada2dee2852e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910190"
---
# <span data-ttu-id="771f3-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="771f3-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="771f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="771f3-102">SYNOPSIS</span></span>
<span data-ttu-id="771f3-103">Удаление профиля журнала.</span><span class="sxs-lookup"><span data-stu-id="771f3-103">Removes a log profile.</span></span>

## <span data-ttu-id="771f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="771f3-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="771f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="771f3-105">DESCRIPTION</span></span>
<span data-ttu-id="771f3-106">Командлет **Remove-AzLogProfile** удаляет профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="771f3-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="771f3-107">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="771f3-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="771f3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="771f3-108">EXAMPLES</span></span>

## <span data-ttu-id="771f3-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="771f3-109">PARAMETERS</span></span>

### <span data-ttu-id="771f3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771f3-110">-DefaultProfile</span></span>
<span data-ttu-id="771f3-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="771f3-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="771f3-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="771f3-112">-Name</span></span>
<span data-ttu-id="771f3-113">Указывает имя профиля, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="771f3-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771f3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="771f3-114">-PassThru</span></span>
<span data-ttu-id="771f3-115">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="771f3-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="771f3-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="771f3-116">-Confirm</span></span>
<span data-ttu-id="771f3-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="771f3-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="771f3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="771f3-118">-WhatIf</span></span>
<span data-ttu-id="771f3-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="771f3-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="771f3-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="771f3-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="771f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771f3-121">CommonParameters</span></span>
<span data-ttu-id="771f3-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="771f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771f3-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="771f3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771f3-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="771f3-124">INPUTS</span></span>

### <span data-ttu-id="771f3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="771f3-125">System.String</span></span>

## <span data-ttu-id="771f3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="771f3-126">OUTPUTS</span></span>

### <span data-ttu-id="771f3-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="771f3-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="771f3-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="771f3-128">NOTES</span></span>

## <span data-ttu-id="771f3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="771f3-129">RELATED LINKS</span></span>

[<span data-ttu-id="771f3-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="771f3-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="771f3-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="771f3-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


