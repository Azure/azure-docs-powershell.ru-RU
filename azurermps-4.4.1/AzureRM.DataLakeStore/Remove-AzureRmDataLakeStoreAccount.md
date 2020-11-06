---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567133"
---
# <span data-ttu-id="03c98-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c98-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="03c98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03c98-102">SYNOPSIS</span></span>
<span data-ttu-id="03c98-103">Удаление учетной записи Data Lake Store без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="03c98-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03c98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03c98-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03c98-105">DESCRIPTION</span></span>
<span data-ttu-id="03c98-106">Командлет **Remove-AzureRmDataLakeStoreAccount** удаляет учетную запись Data Lake Store без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="03c98-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="03c98-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03c98-107">EXAMPLES</span></span>

### <span data-ttu-id="03c98-108">Пример 1: Удаление учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="03c98-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="03c98-109">Эта команда удаляет учетную запись с именем ContosoADL из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03c98-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="03c98-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03c98-110">PARAMETERS</span></span>

### <span data-ttu-id="03c98-111">-Force</span><span class="sxs-lookup"><span data-stu-id="03c98-111">-Force</span></span>
<span data-ttu-id="03c98-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="03c98-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03c98-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03c98-113">-Name</span></span>
<span data-ttu-id="03c98-114">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="03c98-114">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="03c98-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03c98-115">-PassThru</span></span>
<span data-ttu-id="03c98-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="03c98-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03c98-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="03c98-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03c98-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c98-118">-ResourceGroupName</span></span>
<span data-ttu-id="03c98-119">Указывает группу ресурсов, которая содержит учетную запись, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="03c98-119">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="03c98-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03c98-120">-Confirm</span></span>
<span data-ttu-id="03c98-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03c98-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c98-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c98-122">-WhatIf</span></span>
<span data-ttu-id="03c98-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03c98-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c98-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03c98-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c98-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c98-125">-DefaultProfile</span></span>
<span data-ttu-id="03c98-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03c98-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03c98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c98-127">CommonParameters</span></span>
<span data-ttu-id="03c98-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03c98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c98-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c98-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c98-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03c98-130">INPUTS</span></span>

## <span data-ttu-id="03c98-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03c98-131">OUTPUTS</span></span>

### <span data-ttu-id="03c98-132">логических</span><span class="sxs-lookup"><span data-stu-id="03c98-132">bool</span></span>
<span data-ttu-id="03c98-133">Если указана функция PassThru, при успешном завершении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="03c98-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="03c98-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="03c98-134">NOTES</span></span>

## <span data-ttu-id="03c98-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03c98-135">RELATED LINKS</span></span>

[<span data-ttu-id="03c98-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c98-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="03c98-137">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c98-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="03c98-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c98-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="03c98-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c98-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


