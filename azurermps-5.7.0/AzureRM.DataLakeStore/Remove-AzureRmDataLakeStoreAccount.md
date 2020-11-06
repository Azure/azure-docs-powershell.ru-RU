---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 4e21d122c8a49209a7591457c36ba99fcc10496c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559068"
---
# <span data-ttu-id="da52c-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="da52c-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="da52c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da52c-102">SYNOPSIS</span></span>
<span data-ttu-id="da52c-103">Удаление учетной записи Data Lake Store без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="da52c-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da52c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da52c-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da52c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da52c-105">DESCRIPTION</span></span>
<span data-ttu-id="da52c-106">Командлет **Remove-AzureRmDataLakeStoreAccount** удаляет учетную запись Data Lake Store без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="da52c-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="da52c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da52c-107">EXAMPLES</span></span>

### <span data-ttu-id="da52c-108">Пример 1: Удаление учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="da52c-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="da52c-109">Эта команда удаляет учетную запись с именем ContosoADL из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da52c-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="da52c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da52c-110">PARAMETERS</span></span>

### <span data-ttu-id="da52c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da52c-111">-DefaultProfile</span></span>
<span data-ttu-id="da52c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="da52c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da52c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="da52c-113">-Force</span></span>
<span data-ttu-id="da52c-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="da52c-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da52c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da52c-115">-Name</span></span>
<span data-ttu-id="da52c-116">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="da52c-116">Specifies the name of the account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da52c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da52c-117">-PassThru</span></span>
<span data-ttu-id="da52c-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="da52c-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da52c-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="da52c-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da52c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da52c-120">-ResourceGroupName</span></span>
<span data-ttu-id="da52c-121">Указывает группу ресурсов, которая содержит учетную запись, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="da52c-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da52c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da52c-122">-Confirm</span></span>
<span data-ttu-id="da52c-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da52c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da52c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da52c-124">-WhatIf</span></span>
<span data-ttu-id="da52c-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da52c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da52c-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da52c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da52c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da52c-127">CommonParameters</span></span>
<span data-ttu-id="da52c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da52c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da52c-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da52c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da52c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da52c-130">INPUTS</span></span>

### <span data-ttu-id="da52c-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="da52c-131">None</span></span>
<span data-ttu-id="da52c-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="da52c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da52c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da52c-133">OUTPUTS</span></span>

### <span data-ttu-id="da52c-134">логических</span><span class="sxs-lookup"><span data-stu-id="da52c-134">bool</span></span>
<span data-ttu-id="da52c-135">Если указана функция PassThru, при успешном завершении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="da52c-135">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="da52c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="da52c-136">NOTES</span></span>

## <span data-ttu-id="da52c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da52c-137">RELATED LINKS</span></span>

[<span data-ttu-id="da52c-138">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="da52c-138">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="da52c-139">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="da52c-139">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="da52c-140">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="da52c-140">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="da52c-141">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="da52c-141">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


