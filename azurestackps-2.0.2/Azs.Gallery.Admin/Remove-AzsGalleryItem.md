---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076950"
---
# <span data-ttu-id="b2c78-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b2c78-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="b2c78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2c78-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c78-103">Удаление определенного элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="b2c78-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="b2c78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2c78-104">SYNTAX</span></span>

### <span data-ttu-id="b2c78-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2c78-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b2c78-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b2c78-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2c78-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2c78-107">DESCRIPTION</span></span>
<span data-ttu-id="b2c78-108">Удаление определенного элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="b2c78-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="b2c78-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2c78-109">EXAMPLES</span></span>

### <span data-ttu-id="b2c78-110">Пример 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b2c78-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="b2c78-111">Удаление TestUbuntu. Test. 1.0.0 из коллекции стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c78-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="b2c78-112">Пример 2: Remove-AzsGalleryItem через конвейер</span><span class="sxs-lookup"><span data-stu-id="b2c78-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="b2c78-113">Удаляет TestUbuntu. Test. 1.0.0 с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="b2c78-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="b2c78-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2c78-114">PARAMETERS</span></span>

### <span data-ttu-id="b2c78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c78-115">-DefaultProfile</span></span>
<span data-ttu-id="b2c78-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b2c78-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2c78-117">-InputObject</span></span>
<span data-ttu-id="b2c78-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="b2c78-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b2c78-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2c78-119">-Name</span></span>
<span data-ttu-id="b2c78-120">Удостоверение элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="b2c78-120">Identity of the gallery item.</span></span>
<span data-ttu-id="b2c78-121">Содержит имя издателя, имя элемента и может включать версию, разделенную на символ точки.</span><span class="sxs-lookup"><span data-stu-id="b2c78-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b2c78-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2c78-122">-PassThru</span></span>
<span data-ttu-id="b2c78-123">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b2c78-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b2c78-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2c78-124">-SubscriptionId</span></span>
<span data-ttu-id="b2c78-125">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c78-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b2c78-126">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b2c78-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b2c78-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2c78-127">-Confirm</span></span>
<span data-ttu-id="b2c78-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2c78-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c78-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c78-129">-WhatIf</span></span>
<span data-ttu-id="b2c78-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2c78-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c78-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2c78-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c78-132">CommonParameters</span></span>
<span data-ttu-id="b2c78-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2c78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c78-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2c78-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c78-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2c78-135">INPUTS</span></span>

### <span data-ttu-id="b2c78-136">Microsoft. Azure. PowerShell. командлеты. Gallery. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="b2c78-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="b2c78-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2c78-137">OUTPUTS</span></span>

### <span data-ttu-id="b2c78-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2c78-138">System.Boolean</span></span>



## <span data-ttu-id="b2c78-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2c78-139">NOTES</span></span>

<span data-ttu-id="b2c78-140">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b2c78-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2c78-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2c78-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b2c78-142">INPUTOBJECT <IGalleryIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="b2c78-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b2c78-143">`[GalleryItemName <String>]`: Удостоверение элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="b2c78-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="b2c78-144">Содержит имя издателя, имя элемента и может включать версию, разделенную на символ точки.</span><span class="sxs-lookup"><span data-stu-id="b2c78-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="b2c78-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="b2c78-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2c78-146">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c78-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b2c78-147">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="b2c78-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b2c78-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2c78-148">RELATED LINKS</span></span>

