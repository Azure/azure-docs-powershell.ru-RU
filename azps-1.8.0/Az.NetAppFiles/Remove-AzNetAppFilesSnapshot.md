---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 16eb962245502338c7b12f6e5abf20a9bc04b83f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730765"
---
# <span data-ttu-id="b8939-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="b8939-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="b8939-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8939-102">SYNOPSIS</span></span>
<span data-ttu-id="b8939-103">Удаляет снимок NetApp файлов Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="b8939-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="b8939-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8939-104">SYNTAX</span></span>

### <span data-ttu-id="b8939-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8939-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8939-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8939-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8939-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8939-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8939-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8939-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8939-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8939-109">DESCRIPTION</span></span>
<span data-ttu-id="b8939-110">Командлет **Remove-AzNetAppFilesSnapshot** удаляет моментальный снимок ANF.</span><span class="sxs-lookup"><span data-stu-id="b8939-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="b8939-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8939-111">EXAMPLES</span></span>

### <span data-ttu-id="b8939-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8939-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="b8939-113">Эта команда удаляет снимок ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="b8939-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="b8939-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8939-114">PARAMETERS</span></span>

### <span data-ttu-id="b8939-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b8939-115">-AccountName</span></span>
<span data-ttu-id="b8939-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="b8939-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8939-117">-DefaultProfile</span></span>
<span data-ttu-id="b8939-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8939-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8939-119">-InputObject</span></span>
<span data-ttu-id="b8939-120">Удаляемый объект снимка</span><span class="sxs-lookup"><span data-stu-id="b8939-120">The snapshot object to remove</span></span>

```yaml
Type: PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8939-121">-Name</span></span>
<span data-ttu-id="b8939-122">Имя моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="b8939-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8939-123">-PassThru</span></span>
<span data-ttu-id="b8939-124">Возвращает значение, указывающее, был ли успешно удален указанный том</span><span class="sxs-lookup"><span data-stu-id="b8939-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b8939-125">-PoolName</span></span>
<span data-ttu-id="b8939-126">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="b8939-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8939-127">-ResourceGroupName</span></span>
<span data-ttu-id="b8939-128">Группа "ресурсы" для моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="b8939-128">The resource group of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8939-129">-ResourceId</span></span>
<span data-ttu-id="b8939-130">Идентификатор ресурса для моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="b8939-130">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-131">-Тома</span><span class="sxs-lookup"><span data-stu-id="b8939-131">-VolumeName</span></span>
<span data-ttu-id="b8939-132">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="b8939-132">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="b8939-133">-VolumeObject</span></span>
<span data-ttu-id="b8939-134">Объект Volume, содержащий удаляемый снимок.</span><span class="sxs-lookup"><span data-stu-id="b8939-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8939-135">-Confirm</span></span>
<span data-ttu-id="b8939-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8939-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8939-137">-WhatIf</span></span>
<span data-ttu-id="b8939-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8939-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8939-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8939-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8939-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8939-140">CommonParameters</span></span>
<span data-ttu-id="b8939-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8939-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b8939-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8939-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8939-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8939-143">INPUTS</span></span>

### <span data-ttu-id="b8939-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b8939-144">System.String</span></span>

### <span data-ttu-id="b8939-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b8939-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="b8939-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="b8939-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="b8939-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8939-147">OUTPUTS</span></span>

### <span data-ttu-id="b8939-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8939-148">System.Boolean</span></span>

## <span data-ttu-id="b8939-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8939-149">NOTES</span></span>

## <span data-ttu-id="b8939-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8939-150">RELATED LINKS</span></span>
