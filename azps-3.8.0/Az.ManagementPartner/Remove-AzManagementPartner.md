---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911961"
---
# <span data-ttu-id="e40e2-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e40e2-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="e40e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e40e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e40e2-103">Удалите идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="e40e2-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e40e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e40e2-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e40e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e40e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e40e2-106">Удалите идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="e40e2-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e40e2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e40e2-107">EXAMPLES</span></span>

### <span data-ttu-id="e40e2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e40e2-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="e40e2-109">Удаление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="e40e2-109">Remove management partner</span></span>

## <span data-ttu-id="e40e2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e40e2-110">PARAMETERS</span></span>

### <span data-ttu-id="e40e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e40e2-111">-DefaultProfile</span></span>
<span data-ttu-id="e40e2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e40e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e40e2-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="e40e2-113">-PartnerId</span></span>
<span data-ttu-id="e40e2-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="e40e2-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="e40e2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e40e2-115">-PassThru</span></span>
<span data-ttu-id="e40e2-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="e40e2-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e40e2-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e40e2-117">-Confirm</span></span>
<span data-ttu-id="e40e2-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e40e2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e40e2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e40e2-119">-WhatIf</span></span>
<span data-ttu-id="e40e2-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e40e2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e40e2-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e40e2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e40e2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e40e2-122">CommonParameters</span></span>
<span data-ttu-id="e40e2-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e40e2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e40e2-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e40e2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e40e2-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e40e2-125">INPUTS</span></span>

### <span data-ttu-id="e40e2-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="e40e2-126">None</span></span>

## <span data-ttu-id="e40e2-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e40e2-127">OUTPUTS</span></span>

### <span data-ttu-id="e40e2-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e40e2-128">System.Boolean</span></span>

## <span data-ttu-id="e40e2-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e40e2-129">NOTES</span></span>

## <span data-ttu-id="e40e2-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e40e2-130">RELATED LINKS</span></span>

[<span data-ttu-id="e40e2-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e40e2-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="e40e2-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e40e2-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="e40e2-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e40e2-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)