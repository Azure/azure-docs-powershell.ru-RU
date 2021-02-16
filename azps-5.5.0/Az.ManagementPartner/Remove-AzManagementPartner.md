---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219201"
---
# <span data-ttu-id="73bb9-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73bb9-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="73bb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="73bb9-103">Удалите идентификацию текущего пользователя или основной службы Microsoft Partner Network (MPN).</span><span class="sxs-lookup"><span data-stu-id="73bb9-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="73bb9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73bb9-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73bb9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73bb9-105">DESCRIPTION</span></span>
<span data-ttu-id="73bb9-106">Удалите ИД Microsoft Partner Network (MPN) текущего пользователя, который является авториентом или основной службой.</span><span class="sxs-lookup"><span data-stu-id="73bb9-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="73bb9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73bb9-107">EXAMPLES</span></span>

### <span data-ttu-id="73bb9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73bb9-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="73bb9-109">Удаление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="73bb9-109">Remove management partner</span></span>

## <span data-ttu-id="73bb9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73bb9-110">PARAMETERS</span></span>

### <span data-ttu-id="73bb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bb9-111">-DefaultProfile</span></span>
<span data-ttu-id="73bb9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73bb9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73bb9-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="73bb9-113">-PartnerId</span></span>
<span data-ttu-id="73bb9-114">Код партнера по управлению— это 6-значный номер.</span><span class="sxs-lookup"><span data-stu-id="73bb9-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="73bb9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73bb9-115">-PassThru</span></span>
<span data-ttu-id="73bb9-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="73bb9-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="73bb9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73bb9-117">-Confirm</span></span>
<span data-ttu-id="73bb9-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="73bb9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73bb9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73bb9-119">-WhatIf</span></span>
<span data-ttu-id="73bb9-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73bb9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73bb9-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="73bb9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73bb9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bb9-122">CommonParameters</span></span>
<span data-ttu-id="73bb9-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73bb9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bb9-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bb9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bb9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73bb9-125">INPUTS</span></span>

### <span data-ttu-id="73bb9-126">Нет</span><span class="sxs-lookup"><span data-stu-id="73bb9-126">None</span></span>

## <span data-ttu-id="73bb9-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73bb9-127">OUTPUTS</span></span>

### <span data-ttu-id="73bb9-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73bb9-128">System.Boolean</span></span>

## <span data-ttu-id="73bb9-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73bb9-129">NOTES</span></span>

## <span data-ttu-id="73bb9-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73bb9-130">RELATED LINKS</span></span>

[<span data-ttu-id="73bb9-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73bb9-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="73bb9-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73bb9-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="73bb9-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="73bb9-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)