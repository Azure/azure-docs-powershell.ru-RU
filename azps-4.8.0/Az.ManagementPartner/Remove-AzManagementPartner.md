---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079022"
---
# <span data-ttu-id="099d6-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="099d6-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="099d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="099d6-102">SYNOPSIS</span></span>
<span data-ttu-id="099d6-103">Удалите идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="099d6-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="099d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="099d6-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="099d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="099d6-105">DESCRIPTION</span></span>
<span data-ttu-id="099d6-106">Удалите идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="099d6-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="099d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="099d6-107">EXAMPLES</span></span>

### <span data-ttu-id="099d6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="099d6-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="099d6-109">Удаление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="099d6-109">Remove management partner</span></span>

## <span data-ttu-id="099d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="099d6-110">PARAMETERS</span></span>

### <span data-ttu-id="099d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="099d6-111">-DefaultProfile</span></span>
<span data-ttu-id="099d6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="099d6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="099d6-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="099d6-113">-PartnerId</span></span>
<span data-ttu-id="099d6-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="099d6-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="099d6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="099d6-115">-PassThru</span></span>
<span data-ttu-id="099d6-116">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="099d6-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="099d6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="099d6-117">-Confirm</span></span>
<span data-ttu-id="099d6-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="099d6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="099d6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="099d6-119">-WhatIf</span></span>
<span data-ttu-id="099d6-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="099d6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="099d6-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="099d6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="099d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099d6-122">CommonParameters</span></span>
<span data-ttu-id="099d6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="099d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099d6-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="099d6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099d6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="099d6-125">INPUTS</span></span>

### <span data-ttu-id="099d6-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="099d6-126">None</span></span>

## <span data-ttu-id="099d6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="099d6-127">OUTPUTS</span></span>

### <span data-ttu-id="099d6-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="099d6-128">System.Boolean</span></span>

## <span data-ttu-id="099d6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="099d6-129">NOTES</span></span>

## <span data-ttu-id="099d6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="099d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="099d6-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="099d6-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="099d6-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="099d6-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="099d6-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="099d6-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)