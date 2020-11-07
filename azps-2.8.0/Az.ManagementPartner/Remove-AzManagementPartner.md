---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 5910d82ddee49ba47c709a3323f72e325f4067ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720396"
---
# <span data-ttu-id="7ffce-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="7ffce-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="7ffce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ffce-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffce-103">Удалите идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="7ffce-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="7ffce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ffce-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ffce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ffce-105">DESCRIPTION</span></span>
<span data-ttu-id="7ffce-106">Удалите идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="7ffce-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="7ffce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ffce-107">EXAMPLES</span></span>

### <span data-ttu-id="7ffce-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ffce-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="7ffce-109">Удаление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="7ffce-109">Remove management partner</span></span>

## <span data-ttu-id="7ffce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ffce-110">PARAMETERS</span></span>

### <span data-ttu-id="7ffce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffce-111">-DefaultProfile</span></span>
<span data-ttu-id="7ffce-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ffce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ffce-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="7ffce-113">-PartnerId</span></span>
<span data-ttu-id="7ffce-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="7ffce-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="7ffce-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ffce-115">-PassThru</span></span>
<span data-ttu-id="7ffce-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="7ffce-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7ffce-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ffce-117">-Confirm</span></span>
<span data-ttu-id="7ffce-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ffce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ffce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ffce-119">-WhatIf</span></span>
<span data-ttu-id="7ffce-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ffce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ffce-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ffce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ffce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffce-122">CommonParameters</span></span>
<span data-ttu-id="7ffce-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ffce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffce-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffce-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ffce-125">INPUTS</span></span>

### <span data-ttu-id="7ffce-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="7ffce-126">None</span></span>

## <span data-ttu-id="7ffce-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ffce-127">OUTPUTS</span></span>

### <span data-ttu-id="7ffce-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ffce-128">System.Boolean</span></span>

## <span data-ttu-id="7ffce-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ffce-129">NOTES</span></span>

## <span data-ttu-id="7ffce-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ffce-130">RELATED LINKS</span></span>

[<span data-ttu-id="7ffce-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="7ffce-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="7ffce-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="7ffce-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="7ffce-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="7ffce-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)