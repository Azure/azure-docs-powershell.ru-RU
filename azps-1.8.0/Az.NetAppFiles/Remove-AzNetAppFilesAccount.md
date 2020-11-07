---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f59796a51ccd1f3e5e77442cde434ab803d0781
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730767"
---
# <span data-ttu-id="2f6b9-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2f6b9-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="2f6b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f6b9-103">Удаление учетной записи NetApp файлы Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="2f6b9-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="2f6b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f6b9-104">SYNTAX</span></span>

### <span data-ttu-id="2f6b9-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f6b9-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f6b9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f6b9-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f6b9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f6b9-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f6b9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f6b9-108">DESCRIPTION</span></span>
<span data-ttu-id="2f6b9-109">Командлет **Remove-AzNetAppFilesAccount** удаляет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="2f6b9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f6b9-110">EXAMPLES</span></span>

### <span data-ttu-id="2f6b9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="2f6b9-112">Эта команда удаляет учетную запись ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="2f6b9-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="2f6b9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f6b9-113">PARAMETERS</span></span>

### <span data-ttu-id="2f6b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f6b9-114">-DefaultProfile</span></span>
<span data-ttu-id="2f6b9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f6b9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f6b9-116">-InputObject</span></span>
<span data-ttu-id="2f6b9-117">Удаляемый объект учетной записи</span><span class="sxs-lookup"><span data-stu-id="2f6b9-117">The account object to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6b9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f6b9-118">-Name</span></span>
<span data-ttu-id="2f6b9-119">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2f6b9-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6b9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f6b9-120">-PassThru</span></span>
<span data-ttu-id="2f6b9-121">Возвращает значение, указывающее, успешно ли была удалена указанная учетная запись</span><span class="sxs-lookup"><span data-stu-id="2f6b9-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="2f6b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f6b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f6b9-123">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2f6b9-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2f6b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f6b9-124">-ResourceId</span></span>
<span data-ttu-id="2f6b9-125">Идентификатор ресурса для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2f6b9-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="2f6b9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f6b9-126">-Confirm</span></span>
<span data-ttu-id="2f6b9-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f6b9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f6b9-128">-WhatIf</span></span>
<span data-ttu-id="2f6b9-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f6b9-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f6b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6b9-131">CommonParameters</span></span>
<span data-ttu-id="2f6b9-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2f6b9-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f6b9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6b9-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f6b9-134">INPUTS</span></span>

### <span data-ttu-id="2f6b9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2f6b9-135">System.String</span></span>

### <span data-ttu-id="2f6b9-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2f6b9-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2f6b9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f6b9-137">OUTPUTS</span></span>

### <span data-ttu-id="2f6b9-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f6b9-138">System.Boolean</span></span>

## <span data-ttu-id="2f6b9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f6b9-139">NOTES</span></span>

## <span data-ttu-id="2f6b9-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f6b9-140">RELATED LINKS</span></span>
