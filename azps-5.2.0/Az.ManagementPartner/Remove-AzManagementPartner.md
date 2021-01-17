---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329506"
---
# <span data-ttu-id="02844-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="02844-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="02844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02844-102">SYNOPSIS</span></span>
<span data-ttu-id="02844-103">Удалите идентификацию текущего пользователя или основной службы Microsoft Partner Network (MPN).</span><span class="sxs-lookup"><span data-stu-id="02844-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="02844-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02844-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02844-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02844-105">DESCRIPTION</span></span>
<span data-ttu-id="02844-106">Удалите идентификацию текущего пользователя или основной службы Microsoft Partner Network (MPN).</span><span class="sxs-lookup"><span data-stu-id="02844-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="02844-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02844-107">EXAMPLES</span></span>

### <span data-ttu-id="02844-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02844-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="02844-109">Удаление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="02844-109">Remove management partner</span></span>

## <span data-ttu-id="02844-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02844-110">PARAMETERS</span></span>

### <span data-ttu-id="02844-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02844-111">-DefaultProfile</span></span>
<span data-ttu-id="02844-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02844-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02844-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="02844-113">-PartnerId</span></span>
<span data-ttu-id="02844-114">Номер партнера по управлению — 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="02844-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02844-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02844-115">-PassThru</span></span>
<span data-ttu-id="02844-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="02844-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="02844-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02844-117">-Confirm</span></span>
<span data-ttu-id="02844-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="02844-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02844-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02844-119">-WhatIf</span></span>
<span data-ttu-id="02844-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02844-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02844-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="02844-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02844-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02844-122">CommonParameters</span></span>
<span data-ttu-id="02844-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02844-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02844-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02844-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02844-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02844-125">INPUTS</span></span>

### <span data-ttu-id="02844-126">Нет</span><span class="sxs-lookup"><span data-stu-id="02844-126">None</span></span>

## <span data-ttu-id="02844-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02844-127">OUTPUTS</span></span>

### <span data-ttu-id="02844-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02844-128">System.Boolean</span></span>

## <span data-ttu-id="02844-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02844-129">NOTES</span></span>

## <span data-ttu-id="02844-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02844-130">RELATED LINKS</span></span>

[<span data-ttu-id="02844-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="02844-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="02844-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="02844-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="02844-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="02844-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)