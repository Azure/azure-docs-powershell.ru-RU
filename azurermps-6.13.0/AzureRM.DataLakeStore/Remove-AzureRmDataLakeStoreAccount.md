---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 2e73878258a95cf0a7448ba8bfd578e83b69dce6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556692"
---
# <span data-ttu-id="555ad-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="555ad-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="555ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="555ad-102">SYNOPSIS</span></span>
<span data-ttu-id="555ad-103">Удаление учетной записи Data Lake Store без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="555ad-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="555ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="555ad-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="555ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="555ad-105">DESCRIPTION</span></span>
<span data-ttu-id="555ad-106">Командлет **Remove-AzureRmDataLakeStoreAccount** удаляет учетную запись Data Lake Store без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="555ad-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="555ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="555ad-107">EXAMPLES</span></span>

### <span data-ttu-id="555ad-108">Пример 1: Удаление учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="555ad-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="555ad-109">Эта команда удаляет учетную запись с именем ContosoADL из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="555ad-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="555ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="555ad-110">PARAMETERS</span></span>

### <span data-ttu-id="555ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555ad-111">-DefaultProfile</span></span>
<span data-ttu-id="555ad-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="555ad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="555ad-113">-Force</span><span class="sxs-lookup"><span data-stu-id="555ad-113">-Force</span></span>
<span data-ttu-id="555ad-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="555ad-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555ad-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="555ad-115">-Name</span></span>
<span data-ttu-id="555ad-116">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="555ad-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="555ad-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="555ad-117">-PassThru</span></span>
<span data-ttu-id="555ad-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="555ad-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="555ad-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="555ad-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="555ad-121">Указывает группу ресурсов, которая содержит учетную запись, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="555ad-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555ad-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="555ad-122">-Confirm</span></span>
<span data-ttu-id="555ad-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="555ad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="555ad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="555ad-124">-WhatIf</span></span>
<span data-ttu-id="555ad-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="555ad-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="555ad-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="555ad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="555ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555ad-127">CommonParameters</span></span>
<span data-ttu-id="555ad-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="555ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555ad-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="555ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555ad-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="555ad-130">INPUTS</span></span>

### <span data-ttu-id="555ad-131">System. String</span><span class="sxs-lookup"><span data-stu-id="555ad-131">System.String</span></span>

## <span data-ttu-id="555ad-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="555ad-132">OUTPUTS</span></span>

### <span data-ttu-id="555ad-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="555ad-133">System.Boolean</span></span>

## <span data-ttu-id="555ad-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="555ad-134">NOTES</span></span>

## <span data-ttu-id="555ad-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="555ad-135">RELATED LINKS</span></span>

[<span data-ttu-id="555ad-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="555ad-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="555ad-137">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="555ad-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="555ad-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="555ad-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="555ad-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="555ad-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


